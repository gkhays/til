# Docker Compose Restart Policy

```yml
version: "2.1"
services:
  test:
    image: postgres:10.5-alpine
    ports:
      - "5432"
    restart: always
```

## References

1. [Docker-Compose Restart Policy](https://stackoverflow.com/a/42216597/6146580)
1. [How does “restart: always” policy work in docker-compose?](https://serverfault.com/a/884823/544025)
1. [Ensuring Containers Are Always Running with Docker's Restart Policy](https://rollout.io/blog/ensuring-containers-are-always-running-with-dockers-restart-policy/)

Related: `docker run --restart always postgres:10.5-alpine`

[Autostart docker container with systemd](https://dev.to/suntong/autostart-docker-container-with-systemd-5aod)  
[Start containers automatically](https://docs.docker.com/config/containers/start-containers-automatically/)
