# Extract File from Docker Image

```bash
docker create $image  # returns container ID
docker cp $container_id:$source_path $destination_path
docker rm $container_id
```

## References

1. [Exract file from docker image?](https://unix.stackexchange.com/a/370221)
