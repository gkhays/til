# Isolating a Rust Application in a Docker Container

HN user [flatroze](https://news.ycombinator.com/user?id=flatroze) posted a CLI tool for saving web pages as a single file. A comment posted by [mike-cardwell](https://news.ycombinator.com/user?id=mike-cardwell) demonstrated how to compile and run the utility within a Docker container.

Compile and install:

```bash
$ git clone https://github.com/Y2Z/monolith.git
$ cd monolith
$ docker run --rm -w "$(pwd)" -v "$(pwd):$(pwd)" -u "$(id -u):$(id -g)" rust cargo install
```

Now run:

```bash
$ cd target/release
$ docker run --rm -w "$(pwd)" -v "$(pwd):$(pwd)" -u "$(id -u):$(id -g)" rust ./monolith https://www.grepular.com > grepular.html
```

A quick look at `target/release`

```bash
src/monolith/target/release$ ls -la
total 13764
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:33 .
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:22 ..
-rwxrwxrwx 1 ghays ghays        0 Aug 23 11:17 .cargo-lock
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:17 .fingerprint
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:17 build
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:22 deps
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:17 examples
-rw-rw-rw- 1 ghays ghays  1843261 Aug 23 11:34 grepular.html
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:17 incremental
-rwxrwxrwx 1 ghays ghays      221 Aug 23 11:22 libmonolith.d
-rwxrwxrwx 2 ghays ghays  2074980 Aug 23 11:22 libmonolith.rlib
-rwxrwxrwx 2 ghays ghays 10169352 Aug 23 11:22 monolith
-rwxrwxrwx 1 ghays ghays      253 Aug 23 11:22 monolith.d
drwxrwxrwx 1 ghays ghays     4096 Aug 23 11:17 native
```

The same comment poster referenced a [project to isolate node.js](https://gitlab.com/mikecardwell/safernode).

## Running Docker Under WSL

At a quick glance I wasn't sure how to map the volume mounts under Windows and didn't want to take the time, so I set up Docker under WSL. Note: I altered the way the file system mounts -- I changed it from `/mnt/c` to `/c`, e.g.

```bash
ghays@DESKTOP-AQA8MFG:/d/Users/ghays/src/monolith$ df
Filesystem      1K-blocks      Used  Available Use% Mounted on
rootfs          487822332  92280716  395541616  19% /
none            487822332  92280716  395541616  19% /dev
none            487822332  92280716  395541616  19% /run
none            487822332  92280716  395541616  19% /run/lock
none            487822332  92280716  395541616  19% /run/shm
none            487822332  92280716  395541616  19% /run/user
cgroup          487822332  92280716  395541616  19% /sys/fs/cgroup
C:\             487822332  92280716  395541616  19% /c
D:\            1953512444 326810100 1626702344  17% /d
```

To do this, I edited wsl.conf

```bash
sudo vim/etc/wsl.conf

# Now make it look like this and save the file when you're done:
[automount]
root = /
options = "metadata"
```

## References

1. [Show HN: CLI tool for saving web pages as a single file](https://news.ycombinator.com/item?id=20774322)
1. [monolith - Save HTML pages with ease](https://github.com/Y2Z/monolith)
1. [Setting Up Docker for Windows and WSL to Work Flawlessly](https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly)
1. [SaferNode - A safer way to run node](https://gitlab.com/mikecardwell/safernode)
