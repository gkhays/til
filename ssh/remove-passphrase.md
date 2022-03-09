# Remove Passphrase from SSH Key

```bash
ssh-keygen -p
```

One-liner with no prompts.

```bash
ssh-keygen -p [-P old_passphrase] [-N new_passphrase] [-f keyfile]
```

## References

1. [How do I remove the passphrase for the SSH key without having to create a new key?](https://stackoverflow.com/a/112409/6146580)
