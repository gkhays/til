# Troubleshoot Reverse Lookups on Ubuntu 18.04

When executing ... I found the following article: [Reverse Lookups to Local DNS Server Failing on Ubuntu 18.04](https://unix.stackexchange.com/q/584307). I didn't like the solution, but the troubleshooting steps were informative.

```
cat /etc/systemd/resolved.conf
sudo service systemd-resolved status
systemd-resolve --status
```

```
systemctl restart systemd-resolved
```

symlink

```
/etc/resolv.conf -> ../run/systemd/resolve/stub-resolv.conf
```

## References

1. [How to configure systemd-resolved and systemd-networkd to use local DNS server for resolving local domains and remote DNS server for remote domains?](https://unix.stackexchange.com/a/442599)
1. [Ubuntu Configure systemd-resolved](https://serverok.in/systemd-resolved)
1. [New alert keeps showing up: Server returned error NXDOMAIN, mitigating potential DNS violation DVE-2018-0001](https://askubuntu.com/a/1091556/953318)
