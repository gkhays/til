# Display Contents of JAR Manifest

```bash
unzip -q -c myarchive.jar META-INF/MANIFEST.MF
```

Using a single switch.

```bash
unzip -p myarchive.jar META-INF/MANIFEST.MF
```

With Docker Compose.

```bash
docker-compose exec <service_name> unzip -q -c /path/to/myarchive.jar META-INF/MANIFEST.MF
```

With Docker.

```bash
docker exec <container_name> unzip -q -c /path/to/myarchive.jar META-INF/MANIFEST.MF
```

## References

1. [How to read MANIFEST.MF file from JAR using Bash](https://stackoverflow.com/a/7066174/6146580)
