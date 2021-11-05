# List CIDR Blocks in Use

This is really more about learning [JMESPath](https://jmespath.org/) but the AWS CLI gets us off to a good start with `aws ec2 describe-subnets`.

In general you can use an expression of the form:

```bash
aws ec2 describe-subnets --query "Subnets[*].[CidrBlock, SubnetId]" --output table
```

More specifically, you can constrain it to a certain prefix, e.g.

```bash
aws ec2 describe-subnets --query "Subnets[?contains(CidrBlock, '10.10')].[CidrBlock, SubnetId]" --output table
```

Where the output is:

```bash
-----------------------------------------------
|               DescribeSubnets               |
+----------------+----------------------------+
|  10.10.x.0/21  |  subnet-aaa...             |
|  10.10.y.0/21  |  subnet-bbb...             |
|  10.10.0.0/21  |  subnet-ccc...             |
|  10.10.z.0/21  |  subnet-ddd...             |
+----------------+----------------------------+
```

Alternatively

```bash
aws ec2 describe-vpcs --region 'us-east-2' --query 'Vpcs[].CidrBlock'
```

Or with `jq`.

```bash
aws ec2 describe-vpcs --region 'us-east-2' | jq '.Vpcs[].CidrBlock'
```

## References

1. [describe-subnets](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/ec2/describe-subnets.html)
1. [JMESPath is a query language for JSON](https://jmespath.org/)
