# Fix Empty Tuple Error

Within the terraform cache, add an empty array to the `concat()` operation.

```hcl
output "version" {
  value = element(
    concat(
      aws_lambda_function.function_in_vpc_code_in_s3.*.version,
      aws_lambda_function.function_in_vpc_code_in_local_folder.*.version,
      aws_lambda_function.function_not_in_vpc_code_in_s3.*.version,
      aws_lambda_function.function_not_in_vpc_code_in_local_folder.*.version,
      [""], <---------- Fix for empty tuple error
    ),
    0,
  )
}
```

## Related
1. [terraform-aws-lambda v0.8.0](https://github.com/gruntwork-io/package-lambda/releases/tag/v0.8.0)
