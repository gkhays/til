# Dump a Database from a Docker Container

```bash
docker exec <container_name> pg_dump -U <username> -f db_backup.txt <database>
```

Docker Compose invocation.

```bash
docker-compose exec <service_name> pg_dump -U <username> -f db_backup.txt <database>
```

## References

1. [How to generate a Postgresql Dump from a Docker container?](https://stackoverflow.com/a/30171064/6146580)
