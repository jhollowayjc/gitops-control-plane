# Control Plane

## Local Development

### Create a new cluster
```
`kind create cluster --name kind`
```

### Boostrap ArgoCD
```
helm dependency update charts/argocd
helm template argocd charts/argocd --namespace argocd | kubectl apply -f -
```

### Spin up control-plane
```
helm template control-plane charts/control-plane --namespace argocd --values ./clusters/kind/control-plane/values.yaml | kubectl apply -f -
```
