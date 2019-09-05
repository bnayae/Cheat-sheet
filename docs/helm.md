## Docs
[docs](https://helm.sh/docs/)  
[more linkes](https://helm.sh/docs/related/)  

### install

#### Windows

choco install kubernetes-helm  
[see more](https://helm.sh/docs/using_helm/#installing-helm)

helm init  
helm init --force-upgrade  
helm reset --force  
helm version  

#### NGINX Ingress
helm install stable/nginx-ingress --name local-nginx


## Context
Get Context: 
*kubectl config get-contexts*  
Use context: 
*kubectl config use-context docker-desktop*
