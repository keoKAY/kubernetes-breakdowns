## NOTE FOR DEPLOYMENT STRATEGIES 

```bash
cd kubernetes_breakdown/dpl_strategies/blue_green
# . all files inside the folder 
kubectl apply -f . 

kubectl get service 
kubectl get deployment 

# inside service.yaml , edit the replicas:blue to replicas: green 
kubectl apply -f service.yaml 

```