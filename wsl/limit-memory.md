# Limit WSL 2 Memory

Vmmem was spiking to over 99% memory usage. Stop `wsl`.

```console
wsl --shutdown
```

```ini
# https://blog.cloud-eng.nl/2021/02/03/wsl2-limits-vmmem/
[wsl2]
memory=8GB      # How much memory to assign to the WSL 2 VM.
processors=4
swap=1GB
#localhostForwarding=true
```

## References

1. [Configure WSL2 limits on Windows 10](https://blog.cloud-eng.nl/2021/02/03/wsl2-limits-vmmem/)
