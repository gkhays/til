# Analyze a PostgreSQL Database from the Command Line

**Note**: In this example, I am reading in the database connection information from a `YAML` file, as might be used with [Dropwizard](https://www.dropwizard.io/en/stable/).

```bash
command -v psql >/dev/null 2>&1 || { echo >&2 "ERROR: psql not found."; exit 1; }

read -r url user_val password_val <<< "$(yq -r '.database | (.url,.user,.password)' < /config.yml | xargs)"

host=$(echo "$url" | cut -d/ -f3 | cut -d: -f1)
port=$(echo "$url" | cut -d: -f4 | cut -d/ -f1)

user=$(expand_var "$user_val")
password=$(expand_var "$password_val")

PGPASSWORD=$password psql --host="$host" --port="$port" --dbname=postgres --username="$user" -c 'ANALYZE VERBOSE;'
```
