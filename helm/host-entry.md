# Side Effect of the Ingress Host Entry

The `hosts` entry causes an HTTP host header to be added to an AWS ALB listener rule.

```yaml
ingress
  annotgations
  ...
  hosts:
    host: deployed-app.test.net
    paths:
      - path: /
        pathType: prefix
```