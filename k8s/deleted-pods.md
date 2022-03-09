# List Recently Deleted Pods

## References

```bash
kubectl get event -o custom-columns=NAME:.metadata.name | cut -d "." -f1
```

1. [How to list Kubernetes recently deleted pods?](https://stackoverflow.com/a/57309483/6146580)
