# Set the Root Path

In the YAML configuration file you may set the root path under server. The default is `/*`.

```yml
server:
  rootPath: /api/v1/*
```

However, you may also set it in code.

```java
environment.jersey().setUrlPattern("/api/v1/*"); /*or*/
environment.jersey().getResourceConfig().setUrlPattern("/api/v1/*");
```

## References

1. [Dropwizard Configuration Reference](https://www.dropwizard.io/en/latest/manual/configuration.html)
1. [Jersey Environment setUrlPattern no longer works #1408](https://github.com/dropwizard/dropwizard/issues/1408)
1. [Dropwizard Configuration Reference](https://www.dropwizard.io/en/latest/manual/configuration.html)
