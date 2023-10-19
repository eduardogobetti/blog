---
tags:
  - Kubernetes
  - ConfigMap
---

## Imperativa

```shell
kubectl create configmap \
  app-config  --from-literal=APP_COLOR=blue \
              --from-literal=APP_MOD=prod \
```

## Declarativa

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: app-config
data:
  APP_COLOR: blue
  APP_MODE: prod
```