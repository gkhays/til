# Docker Health Check

```yml
services:
  mywebapp:
    # ...
    env_file:
      - ".env"
    healthcheck:
      test: "${DOCKER_HEALTHCHECK_TEST:-curl localhost:8000/healthy}"
      interval: "60s"
      timeout: "3s"
      start_period: "5s"
      retries: 3
```

## References

1. [Docker Tip #85: Define HEALTHCHECK in your Docker Compose File](https://nickjanetakis.com/blog/docker-tip-85-define-healthcheck-in-your-docker-compose-file)
1. [How to Add a Health Check to Your Docker Container](https://howchoo.com/devops/how-to-add-a-health-check-to-your-docker-container)
