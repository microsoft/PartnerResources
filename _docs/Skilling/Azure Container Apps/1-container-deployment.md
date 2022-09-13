---
nav_exclude: true
layout: page
title: Azure Container Apps - Zero to Hero Academy
description: This series will give you a comprehensive introduction Azure Container Apps.
permalink: /skilling/azure-container-apps/1-container-deployment
updated: 2022-09-12
showbreadcrumb: false
tags:
 - azure container apps academy
 - workshop
 - appdev
 - modernize
---

# Hands-On: Getting started with Azure Container Apps

## Content

* [Introduction]({{ site.baseurl }}/skilling/azure-container-apps/intro)
* [Module 1: Hands-On: Getting Started with Azure Container Apps]({{ site.baseurl }}/skilling/azure-container-apps/1-container-deployment)
* [Module 2: Hands-On: Deploying Azure Container Apps with Bicep]({{ site.baseurl }}/skilling/azure-container-apps/2-bicep)
* [Module 3: Hands-On: Routing Traffic to Different Revisions]({{ site.baseurl }}/skilling/azure-container-apps/3-terraform)
* [Module 4: Hands-On: Creating Custom Health Probes with Azure Container Apps]({{ site.baseurl }}/skilling/azure-container-apps/4-probes)

Now that we have covered the general concepts of Azure Container Apps, now it is time to do some hands-on labs and deploy a simple container to Azure Container Apps.

## Install Azure Container Apps extension for Azure CLI

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

## Create an Azure Container App environment with Azure CLI

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

This command will print the FQDN, which we can use in the browser to access NGINX using it’s public address.

![Quickstart]({{ site.baseurl }}/assets/aca-workshop/azure-container-apps-quickstart.jpg)
