
Horizontal Pod Autoscaler 

- Install apache benchmark 
```bash 
   sudo apt-get install apache2-utils
```

```bash 
alias k=kubectl 

kubectl get hpa 
kubectl get pod 
kubectl get service 


ab -n 10000 -c 100 http://10.233.20.159/
```