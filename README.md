# ArgoCD

- Deploy ArgoCD

```bash
  kubectl create namespace argocd

  kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

```bash
  kubectl port-forward -n argocd svc/argocd-server 8080:443
```

```bash
  kubectl get secret argocd-initial-admin-secret -n argocd -o yaml
```

```bash
  echo <password> | base64 --decode
```
