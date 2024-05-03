---
layout: page
title: AI & ML Academy - Azure ML Platform
sorttitle: 05
description: Azure Machine Learning Platform
permalink: /skilling/ai-ml-academy/aml-plat
updated: 2024-05-03
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- academy content
- ai & ml academy module
- ai & ml academy
- aml platform
---

# AI & ML Academy - Azure ML Platform

Welcome to the AI & ML Academy (AIA) - ML Platform!

## Overview
Azure Machine Learning (Azure ML, or AML) Services is a platform and not just a notebook to run ML models. Azure ML Service brings enterprise users the ability to train, test, and deploy their models across a host of environments to support their machine learning applications. The goal is to run our machine learning models in an evergreen production environment as an application and not solely as a one-time experiment.
 
The purpose of this module is to outline the different run-time environments.  We’ve created a decision matrix and plotted the different Azure Services applicable to Artificial Intelligence or Machine Learning. The matrix will have two spectrums (scenarios): Compute Type and ML Lifecycle. The cells of this matrix will define the options we have across the Azure Platform to deploy and run Machine Learning models. The purpose of this module will be to define where each ML service resides and more importantly, the use case, tools, personas, frameworks, and languages that support them.

The first scenario of Azure ML is the Compute Type. Azure ML is a cross-platform environment that spans from Windows, Linux, and Azure. These run-time environments can be classified into two categories: Hybrid or Cloud. A Hybrid environment is a physical or virtual environment that runs on a workstation or set of servers running in a data center or cloud-hosting. The Cloud for this discussion will be Azure running as a PaaS or SaaS service but is not limited to only Azure.
 
The second scenario of Azure ML is the ML Lifecycle. We have different resource requirements depending on where the model resides in the lifecycle. These two stages of the ML lifecycles are Training/Test or Inference (we've simplified the lifecycles to reduce the complexity for this discussion).
 
Here is the decision matrix outlining the scenarios and the resulting run-time environments. There are four options in this matrix and the environment names will be Developer, Hosted, Unmanaged, and Managed. The main purpose of this matrix is to serve as a learning tool and table of content for this learning resource.

|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **ML Lifecycle**	| **Compute Type**
||**Hybrid**|**Cloud**
|**Training/Testing**|Developer Environment|Hosted Environment
|**Inference**|Unmanaged Environment|Managed Environment
 
 
Here are the definitions for each environment that are part of this matrix. (For simplicity, we've defined four and realize there are other combinations like Multi-cloud, but are focusing on the most prevalent environments)

1. **Developer Environment** -- This is an environment for a Pro-Developer Data Scientist to train and test their models. These models can be run on your local machine, physical or virtual servers, and in an IaaS environment in the cloud. The key criteria is the Data scientist will build out their environment from scratch (OS, Language, Framework and IDE). This provides versatility, but a high degree of maintenance to reproduce your model. The mindset of "it runs on my computer" won't be acceptable so an audit trail will be required at release time.
2. **Unmanaged Environment** -- This environment is an extension of the Developer Environment but migrates it to a production environment that is fully-managed by the end-user.  This gives the end-user all the versatility of the open-source ecosystem and provides the best-of-breed approach. A typical end-user would be an ML Engineer who has a model and set of artifacts ready to deploy to production.
3. **Hosted Environment** -- This environment will utilize a common runtime environment in terms of OS, Languages, Frameworks, and IDEs. The hosted environment is set up and supported by Azure. The most common environment will be set up to ensure versatility but reduce set up time for users. A typical user for this environment is a Data Scientist who may experiment in model development but needs to hand-off their code to experts to deploy into production. A great example of this is Azure ML Notebooks.  
4. **Managed Environment** -- This environment is similar to a PaaS or SaaS Azure service where the developer isn't concerned with the set up of their environment or availability of the service. Their main concern is the scalability of the environment to service the traffic to score the data. Managed environments start to transition from a Data Scientist to a more Low-code option to streamline adoption by Citizen Developers. Managed environments are not typically leveraged by Pro-Developers since they like to build their own through the Software Development Lifecycle.
 
The recommended migration path across lifecycles is defined based on the color of the cells. A Hybrid Environment will typically start with the Developer Environment for training/testing and then deploy to an Unmanaged Environment. This Unmanaged Environment can be hosted in Azure.  There is some crossover, but the versions of software you need to replicate in the Developer Environment will likely not match one in the Managed Environment.  he same holds true with the Cloud Environment and migration from Hosted to Managed.  This is a significant gap since it is not only a match across software versions, but also skills of the ML team.


## Developer Environment

This is an environment for a Pro-Developer Data Scientist to train and test their models. These models can be run on your local machine, physical or virtual servers, and in an IaaS environment in the cloud. The key criteria is the Data scientist will build out their environment from scratch (OS, Language, Framework and IDE). This provides versatility, but a high degree of maintenance to reproduce your model. The mindset of "it runs on my computer" won't be acceptable so an audit trail will be required at release time.

For example, a Pro-Developer Data Scientist -- who wants to run their experiment on their local PC in the WSL Environment -- can set up their environment with the necessary requirements file for their ML experiment. They can leverage VS Code to execute code on an ad-hoc basis for training and exploratory data analysis. There local machine doesn't have enough horsepower, so they migrate their environment to an Azure Data Science VM. The additional GPUs will reduce training runtime. Likewise, they can leverage a LINUX VM directly and create the environment from scratch per their local machine configuration. The typical use case is physical, virtual, or IaaS compute. This compute environment is attached to Azure ML Service through the Python SDK to track, monitor, and register models experiments as required.  

Here are the Azure Services that support AI & ML workloads
1.	Local
2.	Remote Azure VM (VM, ACI, AKS)
3.	ML.NET


|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Local| 100| [Fundamentals of machine learning in the cloud](https://www.youtube.com/watch?v=CtX0GZpWz6M&list=PLLasX02E8BPCL966bJ00oIeOhm7w5ejvt&index=11&ab_channel=MicrosoftAzure) |
|| 200|[Enhance your Azure ML experience with the VS Code extension](https://devblogs.microsoft.com/python/enhance-your-azure-machine-learning-experience-with-the-vs-code-extension/)|
|| 300 |[Train an image classification model with Azure ML](https://github.com/Azure/MachineLearningNotebooks/blob/master/tutorials/image-classification-mnist-data/img-classification-part1-training.ipynb)|
| Remote Azure VM| 100|[Supercharge your Azure ML development with VS Code](https://www.youtube.com/watch?v=YJePRMYCTOM&ab_channel=MicrosoftDeveloper)|
|| 200|[Azure ML in a Day](https://github.com/Azure/azureml-examples/blob/main/tutorials/azureml-in-a-day/azureml-in-a-day.ipynb)|
|| 300 |[Machine Learning Cheat Sheet](https://azure.github.io/azureml-cheatsheets/docs/cheatsheets/python/v1/cheatsheet)|
| ML.NET| 100|[ML.NET Comparison Cheat Sheet](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/data-science-and-machine-learning?context=azure%2Fmachine-learning%2Fcontext%2Fml-context#mlnet)|
|| 200|[On .NET Live -- Adding Machine Learning to your .NET Apps with ML .NET](https://www.youtube.com/watch?v=THVD4nzi8vk&ab_channel=dotnet)|
|| 300 |[ML.NET tutorials](https://learn.microsoft.com/en-us/dotnet/machine-learning/tutorials/?WT.mc_id=dotnet-35129-website)|


## Unmanaged Environment

This environment is an extension of the Developer Environment but migrates it to a production environment that is fully-managed by the end-user.  This gives the end-user all the versatility of the open-source ecosystem and provides the best-of-breed approach. A typical end-user would be an ML Engineer who has a model and set of artifacts ready to deploy to production.

After model selection, they leverage the Azure CLI to deploy the model and environment to a LINUX VM in Azure. The Azure VM will run as the scoring engine (inference) for production applications and/or as an MVP application to monitor model performance.

Here are the Azure Services that support AI & ML workloads
1.  Local Web Service (Docker Image)
2.	Remote VM (Azure VM, Kubernetes, AKS)
3.	Windows ML


|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Local Web Service| 100|[How do you deploy a machine learning model as a web service in Azure?](https://youtu.be/n8h6_Expf38)|
|| 200|[Use a custom container to deploy a model to an online endpoint](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-deploy-custom-container?tabs=cli)|
|| 300 |[Register a model and deploy locally](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/deployment/deploy-to-local/register-model-deploy-local.ipynb)|
| Remote VM| 100|[Model deployment and inferencing with Azure ML](https://www.youtube.com/watch?v=WZ7vS10KPAw&ab_channel=MicrosoftAzure)|
|| 200|[ONNX and Azure ML](https://learn.microsoft.com/en-us/azure/machine-learning/concept-onnx)|
|| 300 |[Deploying a web service to Azure Kubernetes Service (AKS)](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/deployment/production-deploy-to-aks/production-deploy-to-aks.ipynb)|
| Windows ML| 100|[Windows AI](https://learn.microsoft.com/en-us/windows/ai/)|
|| 200|[Image Classification with ML.NET and Windows Machine Learning](https://learn.microsoft.com/en-us/windows/ai/windows-ml/tutorials/mlnet-intro)|
|| 300 |[Windows Machine Learning Samples](https://learn.microsoft.com/en-us/windows/ai/windows-ml/samples)|


## Hosted Environment
This environment will utilize a common runtime environment in terms of OS, Languages, Frameworks, and IDEs. The hosted environment is created and supported by Azure. The most common environment will be utilized to ensure versatility but reduce set up time for users. A typical user for this environment is a Data Scientist who may experiment in model development but needs to hand-off their code to experts to deploy into production. A great example of this is Azure ML Notebooks.

These environments will be created with a preconfigured set of machine learning frameworks, languages, packages and tools. This is to ensure set up time is minimal for end-users.  This environment is typically for a Data Scientist who wants to build machine learning models, but isn't an expert regarding configuration and infrastructure. The simplicity of the environment is a benefit, but the flexibility to build a multitude of models for accuracy may be restrained depending on the configuration of these environments. It is highly recommended to review the configuration so you fully understand the options.

Here are the Azure Services that support AI & ML workloads
1.  DSVM
2.  Synapse Analytics Spark Pools
3.  Synapse Analytics Workspace
4.  Azure Machine Learning Notebooks
5.  Azure Machine Learning Attached Compute
5.  Azure Databricks
6.  HDInsight
 

|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| DSVM| 100|[Data Science VM Overview (DSVM)](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/overview)|
|| 200|[Data Science Tools on DSVM](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/tools-included)||
|| 300|[Samples on DSVM](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-samples-and-walkthroughs)||
| Synapse Analytics Workspace| 100|[Machine Learning Experiences in Azure Synapse](https://www.youtube.com/watch?v=xf3Lej-MWCk&ab_channel=MicrosoftDeveloper)|
|| 200|[Azure AI Services in Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/machine-learning/overview-cognitive-services)||
| Synapse Analytics Spark Pools| 100|[Synapse Analytics Spark Pools overview](https://www.youtube.com/watch?v=SPOQzcbTgvQ&t=136s)||
|| 200|[Build a machine learning app with Apache Spark MLlib and Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/spark/apache-spark-machine-learning-mllib-notebook)||
|| 300 |[SynapseML running on Synapse Analytics Spark Pools](https://github.com/microsoft/SynapseML#synapse-analytics)||
| Azure ML Notebooks| 100|[Azure ML Studio Notebooks](https://www.youtube.com/watch?v=AAj-Fz0uCNk&ab_channel=MicrosoftDeveloper)|
|| 200|[Run Jupyter notebooks in your workspace](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-run-jupyter-notebooks)||
|| 300 |[Image Classification using Notebooks in Azure ML](https://www.youtube.com/watch?v=O5bePha5RiY&t=947s&ab_channel=MicrosoftDeveloper)||
| Azure ML Compute| 100|[Training machine learning models at scale with Azure ML](https://www.youtube.com/watch?v=_N8RXm2QrrM&ab_channel=MicrosoftAzure)|
|| 200|[What is an Azure ML compute instance?](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-instance)|
|| 300 |[Azure ML Training Compute Targets](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-target#training-compute-targets)|
| Databricks| 100|[Azure Databricks overview](https://learn.microsoft.com/en-us/azure/databricks/scenarios/what-is-azure-databricks-ml)|
|| 200|[Deploy models for inference and prediction](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/model-inference/)||
|| 300 |[Model training examples](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/train-model/)||


## Managed Environment

This environment is similar to a PaaS or SaaS Azure service where the developer isn't concerned with the setup of their environment or availability of the service. Their main concern is the scalability of the environment to service the traffic to score the data. Managed environments start to transition from a Data Scientist to a more Low-code option to streamline adoption by Citizen Developers. Managed environments are not typically leveraged by Pro-Developers since they like to build their own through the Software Development Lifecycle.
 
These environments are pre-built environments with varying degrees of model portability. The purpose is to reduce machine learning model development/deployment time. A Database Developer might want to run a batch inference script (T-SQL) to score the new data in the database platform and/or a Data Scientist who needs to wear multiple hats can leverage the Azure ML Service for an end-to-end training and scoring.

Here are the Azure Services that support AI & ML workloads
1.  Applied AI
2.	SQL Server Machine Learning Service
3.  Azure SQL Managed Instance
4.  Azure ML Inference Cluster
5.  Azure ML Attached Compute
6.  Azure ML Managed Endpoints
7.  Azure Batch
8.  SQL Edge
9.  IoT Edge


|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Applied AI| 100|[Azure Applied AI Services overview](https://www.youtube.com/watch?v=M6wxdYQrAnQ&ab_channel=MicrosoftDeveloper)|
|| 200|[Prebuilt AI models in Customer Applications](https://www.youtube.com/watch?v=45we8bNPsBc&ab_channel=MicrosoftDeveloper)|
|| 300 |[Create a Document Intelligence Logic Apps workflow](https://learn.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/tutorial-logic-apps)|
| SQL Server ML Svc| 100|[What is SQL Server Machine Learning Services with Python and R?](https://learn.microsoft.com/en-us/sql/machine-learning/sql-server-machine-learning-services?view=sql-server-ver16)|
| Azure SQL Managed Instance| 100|[Machine Learning Services in Azure SQL Managed Instance](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/machine-learning-services-overview?view=azuresql)|
|| 200|[Key Differences between Managed Instance and SQL Server](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/machine-learning-services-differences?view=azuresql)|
|| 300 |[Linear Regression tutorial for Managed Instance](https://learn.microsoft.com/en-us/sql/machine-learning/tutorials/python-ski-rental-linear-regression?view=azuresqldb-mi-current)|
| Azure ML Inference Compute| 100|[Model Deployment and Inferencing](https://www.youtube.com/watch?v=WZ7vS10KPAw&ab_channel=MicrosoftAzure)|
|| 200|[Compute Targets for Inference](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-target#compute-targets-for-inference)|
|| 300 |[Attach AKS to Azure ML workspace](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-attach-kubernetes-to-workspace?source=recommendations&tabs=cli)|
| Azure ML Managed Endpoint| 100|[Online endpoints and deployments for real-time inference](https://learn.microsoft.com/en-us/azure/machine-learning/concept-endpoints-online?view=azureml-api-2)|
|| 200|[Deploy and score model with online endpoint](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-deploy-managed-online-endpoints?tabs=azure-cli)|
| SQL Edge| 100|[What is Azure SQL Edge](https://www.youtube.com/watch?v=QkuJs7S8e6w&ab_channel=MicrosoftDeveloper)|
|| 200 |[ONNX in SQL Edge](https://learn.microsoft.com/en-us/azure/azure-sql-edge/onnx-overview)|
|| 300|[Deploy and make predictions with an ONNX model](https://learn.microsoft.com/en-us/azure/azure-sql-edge/deploy-onnx)|