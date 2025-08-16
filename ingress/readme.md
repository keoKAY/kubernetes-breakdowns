## NOTE FOR ingress 
> Istio 

```bash

cd host-based 
kubectl apply -f . 

kubectl describe svc earthdx-service
kubectl get ingress 

# to see the linked service for a specific hostname 
kubectl describe ingress <ingress-name> 

```