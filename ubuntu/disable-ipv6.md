# Disable IPv6 in Ubuntu

It is possible that IPv6 on Ubuntu may cause DNS problems. If that is an issue, IPv6 can be disabled with the following steps.

## Using Sysctl

```
net.ipv6.conf.all.disable_ipv6 = 1
net.ipv6.conf.default.disable_ipv6 = 1
net.ipv6.conf.lo.disable_ipv6 = 1
```

On Ubuntu server, also add a line for each interface.

```
net.ipv6.conf.<ifname>.disable_ipv6 = 1
```

Activate with

```
sudo sysctl -p
```

Verify with

```
cat /proc/sys/net/ipv6/conf/all/disable_ipv6
```

If IPv6 persists, create `/etc/rc.local` and add

```bash
#!/bin/bash
# /etc/rc.local

/etc/sysctl.d
/etc/init.d/procps restart

exit 0
```

Remember to make it executable with `chmod 755`.

## Using GRUB

Locate and change the following line from

```
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
```

To

```
GRUB_CMDLINE_LINUX_DEFAULT="ipv6.disable=1 quiet splash"
```

Then

```
sudo update-grub
```

## References

1. [How to disable IPv6 in Ubuntu 14.04?](https://askubuntu.com/a/484487/953318)
1. [How to Disable IPv6 in Ubuntu Server 18.04/16.4 LTS](https://www.configserverfirewall.com/ubuntu-linux/ubuntu-disable-ipv6/)
1. [How to disable IPv6 address on Ubuntu 18.04 Bionic Beaver Linux](https://linuxconfig.org/how-to-disable-ipv6-address-on-ubuntu-18-04-bionic-beaver-linux)
1. [How to Disable IPv6 on Ubuntu Linux](https://itsfoss.com/disable-ipv6-ubuntu-linux/)
