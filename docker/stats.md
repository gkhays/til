# Docker Container Statistics

Docker can provide a live stream of container resource usage statistics.

```
docker stats
```

```
CONTAINER ID        NAME                    CPU %               MEM USAGE / LIMIT     MEM %               NET I/O
  BLOCK I/O           PIDS
5d11b63c6d55        daas-remote_agent_1     0.66%               71.29MiB / 1.945GiB   3.58%               1.49MB / 2.18MB
  0B / 0B             17
83a8c23e4de4        daas-remote_client_1    0.07%               121.4MiB / 1.945GiB   6.10%               66.3kB / 36.3kB
  0B / 0B             28
e0c6a146b6b4        daas-remote_pgadmin_1   0.04%               4.68MiB / 1.945GiB    0.23%               2.48kB / 0B
  0B / 0B             1
5c39aae7fac1        daas-remote_kafka_1     10.05%              1.194GiB / 1.945GiB   61.42%              2.19MB / 1.52MB
  0B / 0B             182
c0204991c3bb        daas-remote_db_1        0.00%               4.453MiB / 1.945GiB   0.22%               56.6kB / 46.6kB
  0B / 0B             15
```

```
docker ps -q | xargs docker stats --no-stream
```

## References

1. [Docker container memory usage](https://stackoverflow.com/a/50183268/6146580)
1. [docker stats](https://docs.docker.com/engine/reference/commandline/stats/)
1. [How to See Memory and CPU Usage for All Your Docker Containers (on CentOS 6)](https://dev.to/rubberduck/how-to-see-memory-and-cpu-usage-for-all-your-docker-containers)
