# Show SSH Key Hashes

The old school hash is MD5. Otherwise, the SHA-256 is shown.

```bash
ssh-keygen -lf ~/.ssh/id_rsa.pub -E md5
```

```bash
4096 MD5:06:99:c0:df:08:a9:a6:53:97:bf:e2:e5:79:97:43:f8 gkh@test.net (RSA)
```

## References

1. [How To: Inspect SSH Key Fingerprints](https://www.unixtutorial.org/how-to-inspect-ssh-key-fingerprints/)
1. [How to compare different SSH fingerprint (public key hash) formats?](https://unix.stackexchange.com/a/408349)
