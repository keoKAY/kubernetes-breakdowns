
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