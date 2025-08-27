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

# configmap 
# cd persistance/configmap/demo2
# kubectl apply -f . 

# hostPath dir 
kubectl apply -f . 
kubectl delete -f . 

```

### Configmap 
```bash
kubectl get configmap 
kubectl get configmap -A

# to see the content of the configmap from CLI 
kubectl describe configmap <name> -n default
sudo kubectl get svc 

```

## Secret
```bash
kubectl get secret 
kubectl get secret -A

```


#### Secret with container registry 

```bash
kubectl create secret docker-registry my-dockerhub-secret \
  --docker-server=https://index.docker.io/v1/ \
  --docker-username=myuser \
  --docker-password=mypassword \
  --docker-email=myemail@example.com

# 
kubectl create secret generic postgres-secret \
   --from-literal=POSTGRES_PASSWORD2='MySecurePassword123'


kubectl get secret 
kubectl get secret <name> -o yaml 
kubectl describe secret <name> 

```

### NFS
```bash
git clone url 
cd kuberbernetes-breakdown/persistance/nfs-ansible 
just --list 
just ping-all
just setup-nfs 

```

## GIT 
```bash
# to pull a new code from git 
git status 
git add .
git stash 
git fetch 
git pull 

```