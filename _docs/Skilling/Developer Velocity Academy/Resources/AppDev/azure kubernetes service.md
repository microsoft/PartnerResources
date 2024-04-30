---
layout: page
title: Azure Kubernetes Service
description: Resources for Azure Kubernetes Service
updated: 2024-01-05
permalink: /skilling/developer-velocity-academy/resources/aks
tags:
- learning plan
- azure
- appdev
- kubernetes
---

# Resources for Azure Kubernetes Service (AKS)

Content is broken down as follows:

* **Fundamentals, Associate, Expert:** content categorized by increasing level of complexity
* **Community resources:** user groups, events, blogs
* **Etc.**

## Fundamentals

* [Introduction to Kubernetes Tutorial](https://kubernetes.io/docs/tutorials/kubernetes-basics/)
* [**eBook:** Phippy Goes to the Zoo: A Kubernetes Story](https://azure.microsoft.com/mediahandler/files/resourcefiles/phippy-goes-to-the-zoo/Phippy%20Goes%20To%20The%20Zoo_MSFTonline.pdf)
* [Introduction to Kubernetes on Azure](https://docs.microsoft.com/en-us/learn/paths/intro-to-kubernetes-on-azure/)

## Associate

* [AKS Core Concepts](https://docs.microsoft.com/en-us/azure/aks/concepts-clusters-workloads)
* [Implement a Code Workflow in your Build Pipeline using Git & GitHub](https://docs.microsoft.com/en-us/learn/modules/implement-code-workflow/)
* [Administer Containers in Azure](https://docs.microsoft.com/en-us/learn/paths/administer-containers-in-azure/)

## Expert

* [AKS Construction Kit](https://azure.github.io/AKS-Construction/)
* [AKS Production Baseline](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/containers/aks/secure-baseline-aks)
* [Architect Compute Infrastructure in Azure](https://learn.microsoft.com/en-us/training/paths/architect-compute-infrastructure/) 
* [Architect Infrastructure Operations in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-infrastructure-operations/)
* [Architect Modern Apps in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-modern-apps/)
* [Architect Network Infrastructure in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-network-infrastructure/)
* [Architect Storage Infrastructure in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-storage-infrastructure/)
* [Kubernetes & Azure Arc Management](https://azurearcjumpstart.io/azure_arc_jumpstart/azure_arc_k8s/)

## Community Resources

* [AKS Roadmap](https://github.com/Azure/AKS/projects/1)
* [AKS Release Notes](https://aka.ms/aks/releasenotes)
* [The AKS Checklist](https://www.the-aks-checklist.com/)
* [KubeCon](https://www.cncf.io/kubecon-cloudnativecon-events/)
* [Kubernetes Meetup](https://www.meetup.com/topics/kubernetes/)
* [GitHub AKS Community](https://github.com/Azure/AKS)
* [Azure Developer Community Blog](https://techcommunity.microsoft.com/t5/azure-developer-community-blog/bg-p/AzureDevCommunityBlog)

## AKS Well-Architected Framework Baseline Implementation 

* [Well-Architected Framework Baseline for AKS](https://github.com/mspnp/aks-baseline)

## Certifications

* [Microsoft Certified: Azure Solutions Architect Expert](https://docs.microsoft.com/en-us/learn/certifications/azure-solutions-architect)
* [Certified Kubernetes Administrator (CKA) Program](https://www.cncf.io/certification/cka/)
* [Certified Kubernetes Application Developer (CKAD) Program](https://www.cncf.io/certification/ckad/)

## Marketplace

* [Zero to Hero with K8s Apps in the Azure Marketplace](https://aka.ms/k8sapps)
* [Prepare your Technical Assets](https://learn.microsoft.com/en-us/azure/marketplace/azure-container-technical-assets-kubernetes)

## Learn Kubernetes & AKS through What The Hack

**[What the Hack](https://aka.ms/wth)** is a set of challenge-based hackathons that can be hosted in-person or virtually via Microsoft Teams.

If you are interested in attending a What The Hack event, contact your Microsoft Partner representative. Alternatively, you can host one yourself using the guidance in the [What The Hack Hosting Guide](https://aka.ms/wthhost).

* **[What The Hack: Intro to Kubernetes](https://microsoft.github.io/WhatTheHack/001-IntroToKubernetes/)**

This intro-level hack will help you get hands-on experience with Docker, Kubernetes, and the Azure Kubernetes Service (AKS) on Microsoft Azure. 

The hack covers containers, what problems they solve, and why Kubernetes is necessary to orchestrate them. You will learn all of the Kubernetes jargon (Ex: pods, services, and deployments, oh my!). By the end, you should have a good understanding of what Kubernetes is and be familiar with how to run it on Azure.

* **[What The Hack: Advanced Kubernetes](https://microsoft.github.io/WhatTheHack/023-AdvancedKubernetes/)**

If you've gone through the **[Intro to Kubernetes WTH](https://microsoft.github.io/WhatTheHack/001-IntroToKubernetes/)**, now you know the jargon. Pods, services, and YAML are second nature to you. This hack will dive into the more advanced features of Kubernetes itself. Unlike the intro-level hack where the challenges build on each other, this hack is more of a "choose your own adventure." Once you get a Kubernetes cluster running with the hack's sample application, you can dive deep into any or all of the covered areas in which you are interested. Topics include Helm, Resiliency, Scaling, GitOps, Service Mesh, and Data Volumes.

* **[What The Hack: AKS](https://microsoft.github.io/WhatTheHack/039-AKSEnterpriseGrade/)**

In the **[Intro To Kubernetes WTH](https://microsoft.github.io/WhatTheHack/001-IntroToKubernetes/)**, you learn the basics of Kubernetes itself. You may know how to deploy a basic cluster, but do you know how to get it ready for production in an Enterprise environment? Kubernetes can run in any cloud or on-premises, but knowing the integration points with the underlying platform is critical.

This hack focuses on the integration between Kubernetes, the Azure Kubernetes Service (AKS), and other Azure services. You will explore how to integrate an AKS cluster into your existing private network and make it secure. This includes configuring policies to limit access to the cluster, configuring secrets with Azure Key Vault, and how to monitor your cluster with Azure's monitoring tools.