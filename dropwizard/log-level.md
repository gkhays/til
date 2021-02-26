# Change Log Level Using Admin Task

```bash
curl -X POST -d "logger=org.stuartgunter.dropwizard&level=INFO" http://localhost:8081/tasks/log-level
```

## References

1. [Dropwizard Logging Config](https://github.com/stuartgunter/dropwizard-logging-config)
1. [Dropwizard Core - Tasks](https://www.dropwizard.io/en/latest/manual/core.html#tasks)
