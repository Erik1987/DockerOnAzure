# DockerOnAzure

## Initializing docker on Azure

// first install azure cli using manual from here: https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt

// install and setup docker

// create container registry on Azure

// follow instructions here: https://docs.microsoft.com/en-us/azure/container-instances/tutorial-docker-compose

// create resource group

$ az group create --name myResourceGroup --location eastus

// create container registry

$ az acr create --resource-group myResourceGroup --name <acrName> --sku Basic
  
// set up access key admin on azure container registy

// copy domain name and password

// login to azure using docker

$ docker login yourregistry.azurecr.io

$ docker image tag imagename:[version] registryname.azurecr.io/imagename:[version] 

// push to registry

$ docker push registryname.azurecr.io/imagename:[version] 

// check this: https://dev.to/amilkardev/denied-requested-access-to-the-resource-is-denied-4ie1

// set a container instance using port mapping

// check logs of a running container

$ az container logs --resource-group myResourceGroup --name mycontainer
$ az container attach --resource-group myResourceGroup --name mycontainer
