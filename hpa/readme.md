
Horizontal Pod Autoscaler 

- Install apache benchmark 
```bash 
   sudo apt-get install apache2-utils
```

```bash 
alias k=kubectl 

cd hpa 
kubectl apply -f . 


kubectl get hpa 
kubectl get pod 
kubectl get service 


ab -n 10000 -c 100 http://10.233.20.159/
```

# if we want configure the windows for scaling down the pods 

```bash
behavior:
  scaleDown:
    stabilizationWindowSeconds: 300  # default 300 seconds (5 minutes)
    policies:
      - type: Pods
        value: 1
        periodSeconds: 60
```