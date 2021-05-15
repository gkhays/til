# Filter API Results with jq

```bash
curl -H "Accept: application/vnd.github.v3+json" https://api.github.com/orgs/gruntwork-io/repos | \
  jq '.[] | select(.url | contains("installer")) | {private: .private, url: .url}'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  186k    0  186k    0     0   156k      0 --:--:--  0:00:01 --:--:--  156k
{
  "private": false,
  "url": "https://api.github.com/repos/gruntwork-io/gruntwork-installer"
}
```

## References

1. [Filter objects based on the contents of a key](https://github.com/stedolan/jq/wiki/Cookbook#filter-objects-based-on-the-contents-of-a-key) (JQ Cookbook)
1. [How to filter an array of objects based on values in an inner array with jq?](https://stackoverflow.com/a/26701851/6146580)
1. [jq Tutorial](https://stedolan.github.io/jq/tutorial/)
1. [jq Manual (development version)](https://stedolan.github.io/jq/manual/)
1. [List organization repositories](https://docs.github.com/en/rest/reference/repos#list-user-repositories)
1. [Check if Git repository is private or public (e.g. for GitHub) using Java](https://stackoverflow.com/a/55142903/6146580)
