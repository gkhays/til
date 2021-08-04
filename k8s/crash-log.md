# Obtain Previous Container's Crash Log

```bash
kubectl logs --previous ${POD_NAME} ${CONTAINER_NAME}
```

## References

1. [Examining pod logs](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-running-pod/#examine-pod-logs)
