# Docker Import

```bash
 docker import ./testing.tar testing:latest \
   -c 'CMD python3 test.py -f ./conf/test.properties'
```

## References

1. [docker import](https://docs.docker.com/engine/reference/commandline/import/)
