## NOTE

Installing helm on your `master1` machine 
```bash 
helm version 
which helm # check the executable path 

# show all release 
helm repo list 
helm list 


# to create chart 
helm create nginx-chart

# to deploy 
helm install nginx-release nginx-chart 
helm uninstall nginx-release 

helm upgrade nginx-release nginx-chart 
helm upgrade nginx-release nginx-chart --install 



```

*** 
- Customize helm chart 
```bash
helm create custom-chart 



# lint
helm lint chart-name
helm template chart-name --values prod-values.yaml
```