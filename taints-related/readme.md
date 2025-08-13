

```bash 
alias k=kubectl 
kubectl get node


kubectl get node --show-labels

# node affinity 
# to create your own label for a specific node 
kubectl label nodes node1 disktype=ssd
kubectl label nodes master1 disktype=ssd 
kubectl label nodes master3 disktype=ssd 

# to check on the labels of your  node 
kubectl get node --show-labels | grep "node1"
kubectl describe node node1 | grep -A 5 "Labels:"
```