# Environment Variables in Dropwizard Configuration

```xml
<dependency>
    <groupId>de.thomaskrille</groupId>
    <artifactId>dropwizard-template-config</artifactId>
    <version>1.5.0</version>
</dependency>
```

```java
@Override
public void initialize(final Bootstrap<Configuration> bootstrap) {
    ...
    bootstrap.addBundle(new TemplateConfigBundle());
    ...
}
```

```yml
server:
  type: simple
  connector:
    type: http
    # replacing environment variables
    port: ${PORT}
logging:
  # with default values too
  level: ${LOG_LEVEL!'WARN'}
  appenders:
    # system properties also work
    - type: ${log_appender!'console'}
```

```java
public class MyApplication extends Application<MyConfiguration> {
    // [...]
    @Override
    public void initialize(Bootstrap<MyConfiguration> bootstrap) {
        // Enable variable substitution with environment variables
        bootstrap.setConfigurationSourceProvider(
                new SubstitutingSourceProvider(bootstrap.getConfigurationSourceProvider(),
                                                   new EnvironmentVariableSubstitutor(false)
                )
        );

    }

    // [...]
}
```

```yml
mySetting: ${DW_MY_SETTING}
defaultSetting: ${DW_DEFAULT_SETTING:-default value}
```

## References

1. [Dropwizard Template Config](https://github.com/tkrille/dropwizard-template-config)
1. [Dropwizard Core - Environment variables](https://www.dropwizard.io/en/latest/manual/core.html#environment-variables)
1. [Overriding server connector config with env variables with dropwizard](https://stackoverflow.com/a/32231630/6146580)

### Related

[Dropwizard 3rd Party Modules](https://modules.dropwizard.io/thirdparty/)  
[Dropwizard configuration file security](https://stackoverflow.com/questions/35553673/dropwizard-configuration-file-security)  
[Encrypted Config Value](https://github.com/palantir/encrypted-config-value)
