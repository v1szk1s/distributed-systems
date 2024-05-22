# Prerequisites
- [minikube](https://k8s-docs.netlify.app/en/docs/tasks/tools/install-minikube/)

# How to run
```
minikube start

kubectl apply -f merged.yaml

minikube tunnel

kubectl get services

echo http://$(kubectl get services | grep if-frontend-service | awk '{print $4 "|" $5}' | cut -d: -f 1 | tr "|" ":")

# open this url inside browser

```
