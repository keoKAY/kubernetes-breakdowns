
## Command working with pods 
```bash 

kubectl api-resources
# nginx-pod.yaml
kubectl apply -f nginx-pod.yaml

# to see information  about the pod 
kubectl get pod 
kubectl get pod -o wide
kubectl get pod -o yaml 

# delete object 
kubectl delete -f <filename.yaml >
kubectl delete <pod-name> 
kubectl delete <object/name>


# to see all resoruces inside the cluster
kubectl get all -A
kubectl get all # get all inside default namespace 
```

## Command with replicas 

```bash 
kubectl apply -f nginx-replica.yaml

# to get pod realtime 
kubectl get pod --watch 
kubectl get pod -w
watch kubectl get pod 

# to delete pod managed by RS
kubectl delete pod/pod-name 
```
## Working with deployment
```bash 
kubectl get deployment 
kubectl get deploy 
kubectl get rs 
kubectl get replicaset 
```

*** 




