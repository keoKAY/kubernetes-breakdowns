## NOTE 

```yaml

kubectl apply -f nginx-deploy.yaml --record
# kubectl apply -f file.yaml --record
# myapp-deploy is the name of the deployment
kubectl annotate deployment myapp-deploy \  
  kubernetes.io/change-cause="Updated image to nginx latest "

# check to see if the upgrade was a success or not 
kubectl rollout status deployment/myapp-deploy

# to see the revision number 
kubectl rollout history deployment/myapp-deploy

# just like you Ctrol+Z
kubectl rollout undo deployment/myapp-deploy
kubectl rollout undo deployment/myapp-deploy --to-revision=2
```