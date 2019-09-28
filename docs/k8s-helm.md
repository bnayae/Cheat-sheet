## Docs
[docs](https://helm.sh/docs/)  
[more linkes](https://helm.sh/docs/related/)  
[Helm Best Practice](https://helm.sh/docs/chart_best_practices/)  

### install

#### Windows

choco install kubernetes-helm  
[see more](https://helm.sh/docs/using_helm/#installing-helm)

helm init  
helm init --upgrade
helm init --force-upgrade  
helm reset --force  
helm version  

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

### Ingress
[Troubleshooting Ingress](https://github.com/kubernetes/ingress-nginx/blob/master/docs/troubleshooting.md)  

kubectl get ing -n {@namespace-of-ingress-resource}  
kubectl describe ing {@ingress-resource-name} -n {@namespace-of-ingress-resource}  
kubectl get pods -n {@namespace-of-ingress-controller}

#### NGNIX Ingress Controller

[NGNIX Ingress Controller](https://hub.kubeapps.com/charts/stable/nginx-ingress)  
helm install stable/nginx-ingress --name @{name}  
helm upgrade --install --name @{name} stable/nginx-ingress

## Aliases

[k Aliases](https://github.com/ahmetb/kubectl-aliases/blob/0533366d8e3e3b3987cc1b7b07a7e8fcfb69f93c/.kubectl_aliases)  