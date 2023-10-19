# Control Plane

```
helm dependency update charts/argocd
helm template argocd charts/argocd --namespace argocd | kubectl apply -f - 

helm install control-plane charts/control-plane --namespace argocd --values ./clusters/kind/control-plane/values.yaml
```

