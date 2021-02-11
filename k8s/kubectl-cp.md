# Copy Files from a Pod

Most simply.

```bash
kubectl cp my-pod:my-file my-file
```

In practice, I had to use the namespace. E.g.

```bash
kubectl cp applications/test-srv-hash:results.csv ./results.csv
```

### Troubleshooting

It turns out that if `tar` is not installed in the container, the operation will fail.

## References

1. [Use "kubectl cp" to Copy Files to and from Kubernetes Pods](https://howchoo.com/kubernetes/kubectl-cp-copy-files-to-from-pods)
1. [How to copy files from kubernetes Pods to local system](Use "kubectl cp" to Copy Files to and from Kubernetes Pods)
