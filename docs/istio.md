# Setup Istio

[istio at GitHub](https://github.com/istio/istio/tree/master/install/kubernetes/helm/istio)   
[istio helm install](https://istio.io/docs/setup/kubernetes/helm-install/)  
[Setup](https://istio.io/docs/setup/kubernetes/)  

## Steps:
### Download latest Istio version:

[istio releaes](https://github.com/istio/istio/releases)  

1. extract into folder  
2. cd to the folder  

### CMD
If a service account has not already been installed for Tiller, install one:  
*kubectl apply -f install/kubernetes/helm/helm-service-account.yaml*  

### Helm repo
Add istio.io chart repository and point to the daily release:  
*helm repo add istio.io https://storage.googleapis.com/istio-prerelease/daily-build/master-latest-daily/charts*  

### install istio 
helm install install/kubernetes/helm/istio-init --name istio-init --namespace istio-system  
helm install install/kubernetes/helm/istio --name istio --namespace istio-system   

- if it fail try to run it again

#### Verify
kubectl get svc -n istio-system  
kubectl get pods -n istio-system

### Istio by default
Set istio as default injected for namespace:

kubectl label namespace {@namespace} istio-injection=enabled  
kubectl get namespace -L istio-injection  

### Set Telemetry

[Istio Telemetry](https://istio.io/docs/tasks/telemetry/)  

### Istio setting options
[All Options](https://istio.io/docs/reference/config/installation-options/)  

helm template --set {@option}.enabled=true install/kubernetes/helm/istio --name istio --namespace istio-system > ./{@option}.yaml
kubectl apply -f ./{@option}.yaml  

### Uninstall 
helm delete --purge istio  
helm delete --purge istio-init  

## Visualizing Your Mesh
[setup](https://istio.io/docs/tasks/telemetry/kiali/)  

### Grafana
Grafana (https://istio.io/docs/tasks/telemetry/using-istio-dashboard/):  
kubectl -n istio-system get svc prometheus  
kubectl -n istio-system get svc grafana  
helm upgrade --recreate-pods --namespace istio-system --set grafana.enabled=true istio install/kubernetes/helm/istio  

### Service Graph
Service Graph (https://istio.io/docs/tasks/telemetry/servicegraph/)  
kubectl -n istio-system get svc servicegraph  
helm upgrade --recreate-pods --namespace istio-system --set servicegraph.enabled=true --set grafana.enabled=true istio install/kubernetes/helm/istio  

kubectl -n istio-system port-forward $(kubectl -n istio-system get pod -l app=servicegraph -o jsonpath='{.items[0].metadata.name}') 8088:8088  

http://localhost:8088/force/forcegraph.html  


### K8s
[Cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
