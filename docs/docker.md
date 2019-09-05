## Cleanup

[clean up](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes) any resources — images, containers, volumes, and networks — that are dangling (not associated with a container)
- *docker system prune*

## Delete 
Remove all unused images, not just dangling ones
- *docker image prune -a*
[doc](https://docs.docker.com/engine/reference/commandline/image_prune/)

## Context
Get Context: 
*kubectl config get-contexts*  
Use context: 
*kubectl config use-context docker-desktop*
