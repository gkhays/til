# List EC2 Instances Filtered by AMI

The one is in my Evernote notebook (from April 2021) but I refer to it frequently so adding it to the TIL!

```bash
aws ec2 describe-instances \
  --filters "Name=instance-state-name,Values=running" "Name=image-id,Values=ami-0cab5d75f06b7601a" \
  --query "Reservations[*].Instances[*].{Instance:InstanceId,Name:Tags[?Key=='Name']|[0].Value,Status:State.Name}" \
  --output table
```

Results:

```bash
------------------------------------------------------------------------
|                           DescribeInstances                          |
+----------------------+------------------------------------+----------+
|       Instance       |               Name                 | Status   |
+----------------------+------------------------------------+----------+
|  i-aaa...            |  dub-step-eks-lamp-services        |  running |
|  i-bbb...            |  dub-step-eks-dogecoin-services    |  running |
+----------------------+------------------------------------+----------+
```

## References

1. [List and filter your resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Filtering.html)
1. [Small Tip: How to use AWS CLI ‘–filter’ parameter](http://blog.xi-group.com/2015/01/small-tip-how-to-use-aws-cli-filter-parameter/)
1. [Filtering AWS CLI output](https://docs.aws.amazon.com/cli/latest/userguide/cli-usage-filter.html)
