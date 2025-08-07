## NOTE 

```yaml

kubectl apply -f nginx-deploy.yaml --record
# kubectl apply -f file.yaml --record

kubectl rollout status deployment/nginx-app-blue
# to see the revision number 
kubectl rollout history deployment/nginx-app-blue

# just like you Ctrol+Z
kubectl rollout undo deployment/myapp-deploy
kubectl rollout undo deployment/myapp-deploy --to-revision=2
```