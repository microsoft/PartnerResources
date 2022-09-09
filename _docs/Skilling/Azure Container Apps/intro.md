---
nav_exclude: true
layout: page
title: Azure Container Apps - Zero to Hero Academy
description: This series will give you a comprehensive introduction Azure Container Apps.
permalink: /skilling/Azure Container Apps/intro
updated: 2022-08-12
showbreadcrumb: false
tags:
 - workshop
 - appdev
 - modernize
---

# Azure Container Apps - Zero to Hero Academy

Welcome to the Azure Container Apps - Zero to Hero Academy. This series will give you a comprehensive introduction to what Azure Container Apps are, which technologies are used to provide our serverless container runtime, and how you can build and run containerized workloads within Azure Container Apps (ACA).

## Content
* Azure Container Apps Introduction
* [Module 1: Hands-On: Getting Started with Azure Container Apps](https://github.com/microsoft/PartnerResources/blob/main/PartnerResources/skilling/Azure Container Apps/skilling/Azure%20Container%20Apps/1-container-deployment)
* [Module 2: Hands-On: Deploying Azure Container Apps with Bicep](https://github.com/microsoft/PartnerResources/blob/main/PartnerResources/skilling/Azure%20Container%20Apps/2-bicep)
* [Module 3: Hands-On: Routing Traffic to Different Revisions](https://github.com/microsoft/PartnerResources/blob/main/PartnerResources/skilling/Azure%20Container%20Apps/3-terraform)
* [Module 4: Hands-On: Creating Custom Health Probes with Azure Container Apps](https://github.com/microsoft/PartnerResources/blob/main/PartnerResources/skilling/Azure%20Container%20Apps/4-probes)
* Ongoing Video Resource - COMING SOON!

## Azure Container Apps Overview

Azure Container Apps enables you to run microservices and containerized applications on a serverless platform. If you want to learn more about Azure Container Apps, consult the [official documentation](https://docs.microsoft.com/en-us/azure/container-apps/).

**Common uses of Azure Container Apps include:**
* Deploying API endpoints
* Hosting background processing applications
* Handling event-driven processing
* Running microservices


**Applications built on Azure Container Apps can dynamically scale based on the following characteristics:**
* HTTP traffic
* Event-driven processing
* CPU or memory load
* Any KEDA-supported scaler

#### Example scenarios for Azure Container Apps:
<div style="text-align: center;">

![](assets/aca-workshop/azure-container-apps-example-scenarios.png)

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

![](assets/aca-workshop/azure-container-apps-containers.png)

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


## Conclusion

Getting started with Azure Kubernetes Services can be challenge for organizations. This is especially true for newcomers or developers who want to focus on solving business requirements instead of tackling and mastering the underlying application platform. With the rise of Azure Container Apps, organizations and individual developers can remain focussed on solving business requirements and deploy cloud-native applications with ease to a fully-managed service offering.

If you want to learn more about Azure Container Apps, consult the [official documentation](https://docs.microsoft.com/en-us/azure/container-apps/).
