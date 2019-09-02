## Azure

### Subscriptions  

az login  

az login --use-device-code  

az login --subscription {@subscription-id} 

az account list --output table  

*set default subscription*  
az account set --subscription {@subscription-id}  

### Docker registray

az acr repository list --name {@repository-name} --output table  

docker login wregisry.azurecr.io -u {@user} -p {@pass}  

docker tag {@image-name}:{@version}-{@env} wregisry.azurecr.io/{@image-name}:{@version}-{@env}    

docker push {@repository-name}.azurecr.io/wk-personal-consultant:{@version}-{@env}  

