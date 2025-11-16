# knative-fluxcd-infra

```bash
kind create cluster
kubectl apply -f cluster/flux-system/gotk-components.yaml
kubectl apply -f cluster/flux-system/gotk-sync.yaml

func build --path function --image docker.io/estromenko/function:1 --verbose
kind load docker-image estromenko/function:1
```
