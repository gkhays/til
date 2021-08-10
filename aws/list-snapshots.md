# List RDS Cluster Snapshots

```bash
aws rds describe-db-cluster-snapshots \
  --db-cluster-identifier db-test \
  --query "DBClusterSnapshots[*].[DBClusterSnapshotIdentifier,SnapshotCreateTime]" \
  --output table
--------------------------------------------------------------------------------
|                          DescribeDBClusterSnapshots                          |
+-----------------------------------------+------------------------------------+
|  v1-level-placeholder                   |  2021-08-09T23:06:36.842000+00:00  |
|  db-test-maintenance-snapshot           |  2021-07-30T21:39:51.517000+00:00  |
|  pre-v1.2.3-snapshot                    |  2021-07-22T19:39:10.695000+00:00  |
|  prepare-pr-2007                        |  2021-06-02T20:13:09.001000+00:00  |
|  prepare-pr-584                         |  2021-06-01T13:04:45.293000+00:00  |
+-----------------------------------------+------------------------------------+
```

## References

1. [describe-db-cluster-snapshots](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/rds/describe-db-cluster-snapshots.html)
