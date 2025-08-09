
# To easy working with the other container registry
```bash
kubectl create secret docker-registry ghcr-secret \
  --docker-server=ghcr.io \
  --docker-username=YOUR_GITHUB_USERNAME \
  --docker-password=YOUR_GITHUB_PERSONAL_ACCESS_TOKEN \
  --docker-email=YOUR_EMAIL

```