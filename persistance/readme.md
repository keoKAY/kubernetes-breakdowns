## NOTE 

Pod -> container -> data 
bind storage -> data 

### HostPath 
Store data from the containers inside any host(node) of your clusters 

```bash
# persistence/hostPath
cd kuberbernetes-breakdowns 
git status
git add . 
git stash 
# to get the updated code 
git fetch 
git pull 

# hostPath dir 
kubectl apply -f . 
kubectl delete -f . 

```