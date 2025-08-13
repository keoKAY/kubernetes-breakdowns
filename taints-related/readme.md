

```bash 
alias k=kubectl 
kubectl get node


kubectl get node --show-labels

# node affinity 
# to create your own label for a specific node 
kubectl label nodes node1 disktype=ssd
# on K3s 
kubectl label nodes master1 disktype=ssd 
kubectl label nodes master3 disktype=ssd 

# to check on the labels of your  node 
kubectl get node --show-labels | grep "node1"
kubectl describe node node1 | grep -A 5 "Labels:"

# to see the pod 
kubectl get pod -o wide 

```

***
## Node  tainting node 
```bash
kubectl get node --show-labels
# taint node 
# kubectl taint nodes <machine-name> <role>:<expression>-

kubectl taint nodes node1 node-role.kubernetes.io/master=:NoSchedule

# untaint
kubectl taint nodes node1 node-role.kubernetes.io/master=:NoSchedule-
kubectl describe node node1 | grep -A 5 "Taints:"

```

## Tolerations
```bash
kubectl taint nodes node2 didicated=database:NoSchedule
```
> `node2` will not accept any pods unless they tolerate `dedicated=database`
- Pod with tolerations 
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: db-pod
spec:
  tolerations:
  - key: "dedicated"
    operator: "Equal"
    value: "database"
    effect: "NoSchedule"
  containers:
  - name: db
    image: postgres
```
