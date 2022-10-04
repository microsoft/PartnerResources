---
layout: page
title: AI & ML Academy - Azure Machine Learning Platform
description: Workshop focused on AI and ML - runtime environments
permalink: /skilling/ai-ml-academy/aml-plat
updated: 2022-09-27
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- workshop
---

# AI & ML Academy - Azure Machine Learning Platform

## Overview
Azure Machine Learning Services is a platform and not just a notebook to run ML models.  AML service brings enterprise users the ability to train, test and deploy their models across a host of environments to support their machine learning applications.  The goal is to run our machine learning models in an evergreen production environment as an application and not only one-time experiments. 
 
The purpose of this module is to outline the different run-time environments.  We’ve setup a decision matrix and plotted the different Azure Services applicable to Artificial Intelligence or Machine Learning.  The matrix will have two spectrums(scenarios): Compute Type and ML Lifecycle.  The cells of this matrix will define the options we have across the Azure Platform to deploy and run Machine Learning models.  The purpose of this module will be to define where each ML service resides and more importantly the use case, tools, personas, frameworks and languages that support them.  

The first scenario of Azure Machine Learning is the Compute Type.  AML is a cross-platform environment that spans from Windows, Linux and Azure.  These run-time environments can be classified into two categories; Hybrid or Cloud.  A Hybrid environment is a physical or virtual environment that runs on a workstation or set of servers running in a Data Center or cloud hosting.  The Cloud for this discussion will be Azure running as a PaaS or SaaS service but is not limited to only Azure.
 
The second scenario of Azure Machine Learning is the ML lifecycle.  We have different resource requirements depending on where the model resides in the lifecycle. These two stages of the ML lifecycles are Training/Test & Inference.  (We've simplified the lifecycles to reduce the complexity for this discussion)
 
Here is the decision matrix outlining the scenarios and the resulting run-time environments.  There are four options in this matrix and the environment names will be Developer, Hosted, Unmanaged and Managed.  The main purpose of this matrix is to serve as a learning tool and table of content for this learning resource.  

|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **ML Lifecycle**	| **Compute Type**
||**Hybrid**|**Cloud**
|**Training/Testing**|Developer Environment|Hosted Environment
|**Inference**|Unmanaged Environment|Managed Environment

 	Training/Testing	Developer Environment	Hosted Environment
 	Inference	Unmanaged Environment	Managed Environment
 
 
Here are the definitions for each environment that are part of this matrix.  (For simplicity we've defined four and realize there are other combination like Multi-cloud but are focusing on the most prevalent environments)

1. **Developer Environment** -- This is an environment for a Pro-Developer Data Scientist to train and test their models.  These models can be run on your local machine, physical or virtual servers and in an IaaS environment in the cloud.  The key criteria is the Data scientist will build out their environment from scratch (OS, Language, Framework and IDE).  This provide versatility but high degree of maintenance to reproduce your model.  The mindset of "It runs on my computer" won't be acceptable so an audit trail will be required at release time.
2. **Unmanaged Environment** -- This environment is an extension of the Developer Environment but migrates it to a production environment that is fully managed by the end-user.  This gives the end-user all the versatility of the open-source ecosystem and provides the best-of-breed approach.  A typical end-user would be a ML Engineer who has a published model and set of artifact to deploy to production.  They will ensure it runs in an evergreen environment across it lifetime to ensure accuracy and availability.
3. **Hosted Environment** -- A hosted environment will utilize a common runtime environment in terms of OS, Languages, Frameworks and IDEs.  The hosted environment is setup and supported by Azure.  The most common environment will be setup to ensure versatility but reduce setup time for these users.  A typical user for this environment is a Data Scientist who might be experts in model development but needs to hand-off their code set to experts to deploy into production.  A great example is Azure ML Notebooks.  
4. **Managed Environment** -- This environment is similar to a PaaS or SaaS Azure service where the developer isn't concerned with setup of their environment or availability of the service.  Their main concern is the scalability of the environment to service the traffic to score the data.  Managed environment start to transition from a Data Scientist to a more Low-code option to streamline adoption by Citizen Developers.  Managed environments are not typically leveraged by Pro-Developers since they like to Build their own thru a Software Development Lifecycle.
 
The recommended migration path across lifecycles are defined based on the color of the cells.  A Hybrid environment will typically start with the developer environment for training/testing and then deploy to an unmanaged environment.  This unmanaged environment can be hosted in Azure but always in virtual environment like AKS.  There is crossover but the versions of software you need to replicate in the Developer environment will not likely match one in the managed environment.  The same holds true with the Cloud Environment and migration from Hosted to Managed.  This is a bigger gap since it is not only a match across software versions but also skill sets of the ML team.
 
The rest of this module will outline the list of ML services that run in each of these environments.  We will provide a set of learning resources for your readiness and adoption.  We hope this overview provides the context you require to utilize these environments based on your machine learning ecosystem.


## Developer Environment
This is an environment for a Pro-Developer to leverage to train and test their models.  These models can be run on your local machine, physical or virtual servers and in a IaaS environment in the cloud.  The key criteria is the Data scientist will build out their environment from scratch (OS, Language, Framework and IDE).  This provides versatility but a high degree of maintenance to reproduce your model.  The mindset of "It runs on my computer" won't be acceptable so an audit trail will be required at release time.
 
Here are the Azure Services that support AI & ML workloads
1.	WSL
2.	ML.NET
3.	Azure VM
4.	Kubernetes
5.	AKS
 
The learning resources will not be a deep dive into how to support and develop in these environments.  The intent is how to deploy AI & ML into these environments.  The set of learning resources are curated to help you get to a level 300 understanding.
 
Resource	Level	Training Assets
|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| WSL| 100||
|| 200||
|| 300 ||
| ML.NET| 100||
|| 200||
|| 300 ||
| Azure VM| 100||
|| 200||
|| 300 ||
