# The Difference Between CMD and ENTRYPOINT

I did not realize that `CMD` and `ENTRYPOINT` could co-exist. My intended outcome was to find out how to leverage the same image to perform an initialization activity prior to starting a container hosted service. Mission accomplished!

```
ENTRYPOINT ["java", "-jar", "lib/service.jar"]
CMD ["foo", "bar"]
```

## References

1. [Understand how CMD and ENTRYPOINT interact - Dockerfile reference](https://docs.docker.com/engine/reference/builder/#understand-how-cmd-and-entrypoint-interact)
1. [What is the difference between CMD and ENTRYPOINT in a Dockerfile?](https://stackoverflow.com/a/21564990/6146580)
1. [Ubuntu Dockerfile](https://github.com/dockerfile/ubuntu/blob/master/Dockerfile)
