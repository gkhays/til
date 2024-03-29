# Browse WSL Files from Windows Explorer

In WSL 2, files may be reached at the UNC path `\\wsl$\<distro>\`, e.g.

```
\\wsl$\Ubuntu-18.04\
```

You may determine the name of your distribution as follows.

```
$ wsl -l -v
  NAME                   STATE           VERSION
* Ubuntu-18.04           Running         2
  openSUSE-Leap-15-1     Stopped         2
  kali-linux             Stopped         2
  docker-desktop         Running         2
  docker-desktop-data    Running         2
  Ubuntu                 Stopped         1
  openSUSE-42            Stopped         1
```

In Windows Explorer.

![Explore WSL](../images/explore-wsl.png)

## References

1. [How to Access Your Linux (WSL) Files in Windows 10](https://www.howtogeek.com/426749/how-to-access-your-linux-wsl-files-in-windows-10/)
1. [Access Linux filesystems in Windows and WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/)
