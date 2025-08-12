
# To easy working with the other container registry
```bash
kubectl create secret docker-registry ghcr-secret \
  --docker-server=ghcr.io \
  --docker-username=keokay \
  --docker-password=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 \
  --docker-email=keokay888@gmail.com

```