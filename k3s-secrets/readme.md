
# To easy working with the other container registry
```bash
kubectl create secret docker-registry ghcr-secret \
  --docker-server=ghcr.io \
  --docker-username=username \
  --docker-password=<your-Password>\
  --docker-email=your-email

```