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

### PV and PVC 
```bash
# check for status Bound 
kubectl get pvc 
kubectl get pv 

```


#### Dynamic provision for nfs 

```bash 
# adding repository 
helm repo add nfs-subdir-external-provisioner https://kubernetes-sigs.github.io/nfs-subdir-external-provisioner/


helm install nfs-subdir-external-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
    --set nfs.server=10.148.0.2 \
    --set nfs.path=/srv/nfs_shared/dynamic_pvc

helm install nfs-subdir-external-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
    --set nfs.server=192.168.56.10 \
    --set nfs.path=/srv/nfs_shared

kubectl get storageclass
kubectl get sc 

helm list 
kubectl get deploy # look for nfs-external-provisioner 
```



#### Create interactive container for testing FQDN 

```bash
kubectl run -it dns-test \
  --rm \
  --image=busybox \
  --restart=Never \
  -- sh

# run to test DNS 
nslookup postgres-statefulset-svc.default.svc.mycluster
nslookup postgres-statefulset-svc.default.svc.cluster.local

```