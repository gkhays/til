# PostgreSQL Is Ready Utility

Previously, when waiting on a PostgreSQL database to become ready, I used the [wait-for-it](https://github.com/vishnubob/wait-for-it) script. But when specifically awaiting a PostgreSQL database, I have switched to [pg_isready](https://www.postgresql.org/docs/current/app-pg-isready.html).

```bash
function check_db() {
    local -r db_host="${1}"
    local -r db_port="${2}"
    local -r timeout=3
    local retries=$timeout

    until pg_isready -h "$db_host" -p "$db_port" > /dev/null 2>&1 || [ "$retries" -eq 0 ]; do
        ((retries--))
        sleep 1
    done
    if [[ "$retries" -eq 0 ]]; then
        echo -e "Database ($db_host:$db_port) is not ready"
        return 1
    fi
}
```

## References

1. https://www.postgresql.org/docs/current/app-pg-isready.html
1. https://github.com/vishnubob/wait-for-it
