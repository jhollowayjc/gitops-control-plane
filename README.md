# Control Plane

```
helm dependency update charts/argocd
helm install argocd charts/argocd --namespace argocd --create-namespace

helm install control-plane charts/control-plane --namespace argocd --values ./clusters/kind/control-plane/values.yaml
```

