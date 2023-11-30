# Compose, Build, and Tag

I knew that `docker-compose` supports a `build` directive which allows you to specify a folder containing a `Dockerfile`. But it turns out there are additional capabilities such as `context` and tagging. The context is useful to include files from the parent of the folder containing the Dockerfile.

```yml
version: "2.1"
services:
  test:
    build:
      context: .
      dockerfile: docker/Dockerfile
    image: gkh/test:1.1
    ports:
      - "8080:8080"
      - "8085:8085"
```

To build the image:

```console
docker-compose build
```

## References

1. [docker-compose build](https://docs.docker.com/compose/reference/build/)
1. [Compose file version 3 reference - build](https://docs.docker.com/compose/compose-file/#build)
1. [What is the difference between `docker-compose build` and `docker build`?](https://stackoverflow.com/a/50230608/6146580)
