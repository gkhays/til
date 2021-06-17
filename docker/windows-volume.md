# Volume Mounts on Windows

```console
docker run --rm -it -v %cd%:/usr/src/project gcc:4.9
```

In PowerShell, use `${PWD}` (current dir).

```ps1
docker run --rm -it -v ${PWD}:/usr/src/project gcc:4.9
```

On Linux.

```bash
docker run --rm -it -v $(pwd):/usr/src/project gcc:4.9
```

Both Linux and PowerShell.

```bash
docker run --rm -it -v ${PWD}:/usr/src/project gcc:4.9
docker run --rm -it -v $(pwd):/usr/src/project gcc:4.9
```

For Git Bash, add a leading `/`.

```bash
docker run -p 3000:3000 -v /app/node_modules -v /$(pwd):/app 09b10e9fda85
```

## References

1. [Mount current directory as a volume in Docker on Windows 10](https://stackoverflow.com/a/41489151/6146580)
1. [docker --volume format for Windows](https://stackoverflow.com/a/56975849/6146580)
