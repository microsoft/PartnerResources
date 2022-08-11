---
nav_exclude: true
layout: page
title: Azure Container Apps - Zero to Hero
description: Learn Azure Container Apps with hands on labs, and reference material
permalink: /skilling/Azure Container Apps/intro
updated: 2022-08-11
showbreadcrumb: false
tags: 
 - workshop
 - appdev
 - modernization
---
This series will give you a comprehensive introduction to what Azure Container Apps are, which technologies are used to provide our serverless container runtime, and how you can build and run containerized workloads within Azure Container Apps (ACA) 

## Azure Container Apps Overview 

Azure Container Apps enables you to run microservices and containerized applications on a serverless platform. 

Common uses of Azure Container Apps include:
* Deploying API endpoints
* Hosting background processing applications
* Handling event-driven processing
* Running microservices


Applications built on Azure Container Apps can dynamically scale based on the following characteristics:
* HTTP traffic
* Event-driven processing
* CPU or memory load
* Any KEDA-supported scaler

#### Example scenarios for Azure Container Apps:
<div style="text-align: center;">

![](/assets/aca-workshop/azure-container-apps-example-scenarios.png)

</div>

Azure Container Apps enables executing application code packaged in any container and is unopinionated about runtime or programming model. With Container Apps, you enjoy the benefits of running containers while leaving behind the concerns of managing cloud infrastructure and complex container orchestrators.

### Scaling in Azure Container Apps with KEDA

[Kubernetes Event-driven Autoscaling (KEDA)](https://keda.sh/) builds the foundation for all-the-things scaling in Azure Container Apps. Whether you want to scale on compute metrics such as memory or CPU alLOCATION or if you need to scale a specific workload based on messages being stored in a queue.


### Microservice in Azure Container Apps with Dapr

[Distributed Application Runtime (dapr)](https://dapr.io/) lets you build and connect microservices with ease. Dapr allows you to build loosely-coupled microservice architectures instead of creating the next distributed monolith.

In Azure Container Apps we leverage Dapr and its components to build applications with resilience, scalability, and loose coupling in mind.

### Advanced network capabilities with Envoy

Incoming HTTP requests are routed through an [Envoy proxy](https://www.envoyproxy.io/), mostly hidden from the users of Azure Container Apps. However, having a powerful proxy as part of the platform allows us to configure powerful features such as traffic routinfor blue/green deployments and A/B testing with ease. 

### Upgrade to full-fledged Azure Kubernetes Service

You can upgrade from Azure Container Apps to full-fledged Azure Kubernetes Service (AKS) at any time and unleash the full power of Kubernetes.

## Core Components of Azure Container Apps

Azure Container Apps comes with a handful of components that you will need to understand and know how to properly leverage to build cloud-native enterprise applications. The image below is a high-level example of a few applications/containers deployed to the Azure Container Apps environment. 

<div style="text-align: center;">

![](/assets/aca-workshop/azure-container-apps-containers.png)

</div>

### Containers in Azure Container Apps

You run containers in Azure Container Apps. It can consume those containers from public registries like Docker Hub or private registries like Azure Container Registry (ACR). When consuming container images from private registries, corresponding credentials must be provided as part of the application template.

We do not deploy containers directly. Like _Kubernetes_, Azure Container Apps uses _Pods_ as an atomic vehicle to run containers. We can define _Pods_ to consist of multiple containers. In _Kubernetes_, we call this a sidecar pattern. All containers of a _Pod_ share hard disk and network resources. Currently, Azure Container Apps supports Linux-based containers only.

### Revisions in Azure Container Apps

A _revision_ represents an immutable snapshot of a Pod. There is at least one _revision_, which is created automatically during initial deployment. Typically, we will have multiple revisions of a _Pod_ at a certain point in time to provide A/B testing or Blue/Green deployments. New _revisions_ will be generated automatically when containers change or modifications are made to the `template` section of a _Pod_. Consider reviewing the [different change types](https://docs.microsoft.com/en-us/azure/container-apps/revisions#change-types), to understand which modifications will result in new revisions being created automatically by Azure Container Apps.

### Container Apps in Azure Container Apps

A _container app_ consists of at least one _revision_. Every _container app_ can have active and inactive revisions. However, it has at least one active revision. If a revision is not needed anymore, we can deactivate the revision. (We can also re-activate inactive revisions)

### Environments in Azure Container Apps

An _environment_ consists of at least one _container app_. Every _environment_ acts as a security boundary, which means all its _container apps_ are deployed into a dedicated _Azure Virtual Network_. All logs produced from containers inside of the _environment_ are sent to a dedicated _Azure Log Analytics Workspace_.

## Hands-On: Getting started with Azure Container Apps

Now that we have covered the general concepts of Azure Container Apps, now it is time to do some hands-on labs and deploy a simple container to Azure Container Apps.

### Install Azure Container Apps extension for Azure CLI

To get started we will have to install the Azure Container Apps extension for Azure CLI. Once we have installed the extension, we will have access to the `az containerapp` sub-command.

First, sign in to Azure from the CLI. Run the following command, and follow the prompts to complete the authentication process.

```
# Sign into Azure CLI 
az login
```
Next, install the Azure Container Apps extension for the CLI.

```
# Install Azure Container Apps CLI extension
az extension add --name containerapp --upgrade
```
Now that the extension is installed, register the Microsoft.App namespace.

```
az provider register --namespace Microsoft.App
```

Register the Microsoft.OperationalInsights provider for the Azure Monitor Log Analytics Workspace if you have not used it before.  If you are currently using Log Analytics or Azure Monitor you can skip this step.  

```
az provider register --namespace Microsoft.OperationalInsights
```

### Create an Azure Container App environment with Azure CLI

The following snippet creates all necessary components, including Azure Resource Group and Azure Log Analytics Workspace. You can modify the deployment by changing the variables located at the beginning of the snippet:

```
# variables
LOCATION="westus2"
RESOURCE_GROUP="rg-containerapps"
LA_WRKSPACE="logwrkspace2"
CONTAINERAPPS_ENVIRONMENT="partner-sample2"

# Create Resource Group
az group create -n $RESOURCE_GROUP -l $LOCATION

# Create Log Analytics Workspace
az monitor log-analytics workspace create \
 -n $LA_WRKSPACE \
 -g $RESOURCE_GROUP

# Grab Log Analytics Workspace ClientId
lawClientId=$(az monitor log-analytics workspace show \
 --query customerId \
 -g $RESOURCE_GROUP \
 -n $LA_WRKSPACE \
 --out tsv)

# Grab Log Analytics Workspace ClientSecret
lawClientSecret=$(az monitor log-analytics workspace get-shared-keys --query primarySharedKey \
 -g $RESOURCE_GROUP \
 -n $LA_WRKSPACE \
 --out tsv)

# Create Azure Container App Environment
az containerapp env create \
 -n $CONTAINERAPPS_ENVIRONMENT \
 -g $RESOURCE_GROUP \
 --logs-workspace-id $lawClientId \
 --logs-workspace-key $lawClientSecret \
 -l $LOCATION
```

## Deploy a Container to Azure Container Apps with Azure CLI

Now that we have an environment in place, we can deploy a container app. For demonstration purpose, we will use our Hello World example from the Azure Container Registry:

```
# Deploy NGINX to Azure Container Apps
az containerapp create \
 -n sample-nginx\
 -g $RESOURCE_GROUP\
 --environment $CONTAINERAPPS_ENVIRONMENT\
 --image mcr.microsoft.com/azuredocs/containerapps-helloworld:latest \ \
 --target-port 80 \
 --ingress 'external' \
 --query configuration.ingress.fqdn
```

The above command will print the FQDN, which we can use in the browser to access the Hello World example..

<div style="text-align: center;">

![](/assets/aca-workshop/azure-container-apps-quickstart.jpg)

</div>

## Conclusion

Getting started with Kubernetes can be challenge for organizations. This is especially true for newcomers or developers who want to focus on solving business requirements instead of tackling and mastering the underlying application platform. With the rise of Azure Container Apps, organizations and individual developers can remain focussed on solving business requirements and deploy cloud-native applications with ease to a fully-managed service offering.

If you want to learn more about Azure Container Apps, consult the [official documentation](https://docs.microsoft.com/en-us/azure/container-apps/).
