## Docs
[docs](https://helm.sh/docs/)  
[more linkes](https://helm.sh/docs/related/)  

### install

#### Windows

choco install kubernetes-helm  
[see more](https://helm.sh/docs/using_helm/#installing-helm)

helm init  
helm init --upgrade
helm init --force-upgrade  
helm reset --force  
helm version  

#### NGINX Ingress
helm install stable/nginx-ingress --name local-nginx

## K8s Cheat Sheet  

[Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)  

## Context
Get Context: 
**kubectl config get-contexts**  
Use context: 
**kubectl config use-context docker-desktop**  

## Context under namespace
**kubectl get namespace**  
Use context with default naemspace:  
**kubectl config set-context --current --namespace={@namespace}**  
Validate:  
**kubectl config view | grep namespace:**
