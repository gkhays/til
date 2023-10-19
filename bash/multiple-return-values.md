# Get Multiple Values from a Bash Function

`yq` does a great job of parsing and extracting values from `YAML` files. However, it typically outputs the results on separate lines. If we can get them on the same line(`xargs` to the rescue), we can use "Here Document" or `HereDoc` to extract them into variables.

```bash
read -r url user password <<< "$(yq -r '.database | (.url,.user,.password)' < /conf/config.yml | xargs)"
```

**Note**: Later versions of `yq` may not have the `-r` shortcut, in which case you must use the longer form `--unwrapScalar`.

Here is a snippet of the `YAML` file.

```yaml
---
# Database settings.
database:
  driverClass: org.h2.Driver
  user: sa
  password: sa
  url: jdbc:h2:./target/example
```

## References

1. [Returning Multiple Values (“Tuples”-ish) from Bash Functions](https://www.assertnotmagic.com/2020/06/19/bash-return-multiple/)
