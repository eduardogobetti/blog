---
tags:
  - Kubernetes
  - Deployment
---

## Imperativa

```shell
kubectl create -f deployment-definition.yml
kubectl get deployments
kubectl get replicaset
kubectl get pods
```


## Declarativa

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-deployment
  labels:
    name: myapp
    type: front-end
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx
  replicas: 3
  selector:
    matchLabels:
      type: front-end
```
