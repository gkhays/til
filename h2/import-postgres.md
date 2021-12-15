# Import Data to H2 From PostgreSQL

Export a table from a PostgreSQL database into CSV and then import the CSV into a table in an H2 database.

### PostgreSQL

Using the `COPY` statement. The `HEADER` flog exports the column names.

```sql
COPY persons TO '/tmp/people.csv' with csv;
```

Alternatively, use the `\copy` command.

```bash
\copy (SELECT * FROM persons) to '/tmp/people.csv' with csv
```

A more complex example.

```bash
psql --host $DB_HOST --dbname $DB_NAME --username=$DBA_USER \
  -c "\copy (SELECT \
    d.name, \
    s.id,s.data_thing, \
    p.data_producer_type, \
    p.start_time, \
    p.end_time, \
    p.end_time - p.start_time as elapsed \
  from data_producer d, sversion s, data_thing p \
  where s.data_producer=d.id and s.data_thing=p.id \
  order by p.end_time) \
  to 'data_prod.csv' with csv header;"
```

### H2

Read using the `CSVREAD` function.

```sql
SELECT * FROM CSVREAD('test.csv');
```

Import data from a CSV file.

```sql
CREATE TABLE TEST AS SELECT * FROM CSVREAD('test.csv');
CREATE TABLE TEST(ID INT PRIMARY KEY, NAME VARCHAR(255))
    AS SELECT * FROM CSVREAD('test.csv');
```

### From a Docker Container

```bash
dc exec db psql --dbname bridge --username postgres -c "\copy (SELECT * FROM credential) to 'cred_export.csv' with csv
 header;"
COPY 6

docker cp agent_db_1:cred_export.csv cred_export.csv
```

## References

1. [Export PostgreSQL Table to CSV File](https://www.postgresqltutorial.com/export-postgresql-table-to-csv-file/)
1. [CSV (Comma Separated Values) Support](http://www.h2database.com/html/tutorial.html?highlight=csv&search=csv#csv)
