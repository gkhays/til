# Export Tables to CSV

```sql
psql -c "\copy (SELECT * FROM account) to '/tmp/account.csv' with csv;"
```

## References

1. [How to export all tables in a PostgreSQL database to csv files?](https://stackoverflow.com/a/66138909/6146580)
