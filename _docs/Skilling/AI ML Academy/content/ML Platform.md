---
layout: page
title: AI & ML Academy - Azure Machine Learning Platform
sorttitle: 05
description: Azure Machine Learning Platform
permalink: /skilling/ai-ml-academy/aml-plat
updated: 2024-05-01
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

# AI & ML Academy - Azure Machine Learning Platform

Welcome to the AI & ML Academy (AIA) - ML Platform!

## Overview
Azure Machine Learning Services is a platform and not just a notebook to run ML models.  AML service brings enterprise users the ability to train, test and deploy their models across a host of environments to support their machine learning applications.  The goal is to run our machine learning models in an evergreen production environment as an application and not only one-time experiments. 
 
The purpose of this module is to outline the different run-time environments.  We’ve set up a decision matrix and plotted the different Azure Services applicable to Artificial Intelligence or Machine Learning.  The matrix will have two spectrums(scenarios): Compute Type and ML Lifecycle.  The cells of this matrix will define the options we have across the Azure Platform to deploy and run Machine Learning models.  The purpose of this module will be to define where each ML service resides and more importantly the use case, tools, personas, frameworks and languages that support them.  

The first scenario of Azure Machine Learning is the Compute Type.  AML is a cross-platform environment that spans from Windows, Linux and Azure.  These run-time environments can be classified into two categories; Hybrid or Cloud.  A Hybrid environment is a physical or virtual environment that runs on a workstation or set of servers running in a Data Center or cloud hosting.  The Cloud for this discussion will be Azure running as a PaaS or SaaS service but is not limited to only Azure.
 
The second scenario of Azure Machine Learning is the ML lifecycle.  We have different resource requirements depending on where the model resides in the lifecycle. These two stages of the ML lifecycles are Training/Test & Inference.  (We've simplified the lifecycles to reduce the complexity for this discussion)
 
Here is the decision matrix outlining the scenarios and the resulting run-time environments.  There are four options in this matrix and the environment names will be Developer, Hosted, Unmanaged and Managed.  The main purpose of this matrix is to serve as a learning tool and table of content for this learning resource.  

|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **ML Lifecycle**	| **Compute Type**
||**Hybrid**|**Cloud**
|**Training/Testing**|Developer Environment|Hosted Environment
|**Inference**|Unmanaged Environment|Managed Environment
 
 
Here are the definitions for each environment that are part of this matrix.  (For simplicity we've defined four and realize there are other combinations like Multi-cloud but are focusing on the most prevalent environments)

1. **Developer Environment** -- This is an environment for a Pro-Developer Data Scientist to train and test their models.  These models can be run on your local machine, physical or virtual servers and in an IaaS environment in the cloud.  The key criteria is the Data scientist will build out their environment from scratch (OS, Language, Framework and IDE).  This provides versatility but high degree of maintenance to reproduce your model.  The mindset of "It runs on my computer" won't be acceptable so an audit trail will be required at release time.
2. **Unmanaged Environment** -- This environment is an extension of the Developer Environment but migrates it to a production environment that is fully managed by the end-user.  This gives the end-user all the versatility of the open-source ecosystem and provides the best-of-breed approach.  A typical end-user would be a ML Engineer who has a published model and set of artifact to deploy to production.  They will ensure it runs in an evergreen environment across it lifetime to ensure accuracy and availability.
3. **Hosted Environment** -- A hosted environment will utilize a common runtime environment in terms of OS, Languages, Frameworks and IDEs.  The hosted environment is set up and supported by Azure.  The most common environment will be set up to ensure versatility but reduce setup time for these users.  A typical user for this environment is a Data Scientist who might be experts in model development but needs to hand-off their code set to experts to deploy into production.  A great example is Azure ML Notebooks.  
4. **Managed Environment** -- This environment is similar to a PaaS or SaaS Azure service where the developer isn't concerned with setup of their environment or availability of the service.  Their main concern is the scalability of the environment to service the traffic to score the data.  Managed environments start to transition from a Data Scientist to a more Low-code option to streamline adoption by Citizen Developers.  Managed environments are not typically leveraged by Pro-Developers since they like to Build their own thru a Software Development Lifecycle.
 
The recommended migration path across lifecycles is defined based on the color of the cells.  A Hybrid environment will typically start with the developer environment for training/testing and then deploy to an unmanaged environment.  This unmanaged environment can be hosted in Azure but always in virtual environment like AKS.  There is crossover but the versions of software you need to replicate in the Developer environment will not likely match one in the managed environment.  The same holds true with the Cloud Environment and migration from Hosted to Managed.  This is a bigger gap since it is not only a match across software versions but also skill sets of the ML team.
 
The rest of this module will outline the list of ML services that run in each of these environments.  We will provide a set of learning resources for your readiness and adoption.  We hope this overview provides the context you require to utilize these environments based on your machine learning ecosystem.


## Developer Environment
This is an environment for a Pro-Developer Data Scientist to train and test their models.  These models can be run on your local machine, physical or virtual servers and in an IaaS environment in the cloud.  The key criteria is the data scientists will build out their environment from scratch (OS, Language, Framework and IDE).  This provides versatility but a high degree of maintenance to reproduce your model.  The mindset of "It runs on my computer" won't be acceptable so an audit trail will be required at release time.

For example, a data scientist wants to run their experiment on their local PC in the WSL environment can set up their conda environment with the necessary requirements file for their machine learning experiment.  They can leverage VS code to execute this code on an ad-hoc basis for training and exploratory data analysis.  There local machine doesn't have enough horsepower, so they migrate their environment to an Azure Data Science VM.  The additional GPUs will reduce training runtime.  Likewise, they can leverage a LINUX VM directly and setup the environment from scratch per their local machine configuration.  The typical use case is physical, virtual or IaaS compute.  This compute environment is attached to Azure Machine Learning Service through the Python SDK to track, monitor and register models experiments as required.  

Here are the Azure Services that support AI & ML workloads
1.	Local
2.	Remote Azure VM (VM, ACI, AKS)
3.	ML.NET

 
The learning resources will not be a deep dive into how to support and develop in these environments.  The intent is how to deploy AI & ML into these compute environments.  The set of learning resources are curated to help you get to a level 300 understanding.
 



|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Local| 100| [Fundamentals of machine learning in the cloud](https://www.youtube.com/watch?v=CtX0GZpWz6M&list=PLLasX02E8BPCL966bJ00oIeOhm7w5ejvt&index=11&ab_channel=MicrosoftAzure) |
|| 200|[Enhance your Azure Machine Learning experience with the VS Code extension](https://devblogs.microsoft.com/python/enhance-your-azure-machine-learning-experience-with-the-vs-code-extension/)|
|| 300 |[Train an image classification model with Azure Machine Learning](https://github.com/Azure/MachineLearningNotebooks/blob/master/tutorials/image-classification-mnist-data/img-classification-part1-training.ipynb)|
| Remote Azure VM| 100|[Supercharge Your Azure ML Development Through Visual Studio Code](https://www.youtube.com/watch?v=YJePRMYCTOM&ab_channel=MicrosoftDeveloper)|
|| 200|[AzureML in a Day](https://github.com/Azure/azureml-examples/blob/main/tutorials/azureml-in-a-day/azureml-in-a-day.ipynb)|
|| 300 |[Machine Learning Cheat Sheet](https://azure.github.io/azureml-cheatsheets/docs/cheatsheets/python/v1/cheatsheet)|
| ML.NET| 100|[ML.NET Comparison Sheet](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/data-science-and-machine-learning?context=azure%2Fmachine-learning%2Fcontext%2Fml-context#mlnet)|
|| 200|[On .NET Live - Adding Machine Learning to your .NET Apps with ML .NET](https://www.youtube.com/watch?v=THVD4nzi8vk&ab_channel=dotnet)|
|| 300 |[ML.NET tutorialsi](https://learn.microsoft.com/en-us/dotnet/machine-learning/tutorials/?WT.mc_id=dotnet-35129-website)|




## Unmanaged Environment
This environment is an extension of the Developer Environment but migrates it to a production environment that is fully managed by the end-user.  This gives the end-user all the versatility of the open-source ecosystem and provides the best-of-breed approach.  A typical end-user would be a ML Engineer who has a published model and set of artifact to deploy to production.  They will ensure it runs in an evergreen environment across it lifetime to ensure accuracy and availability.

After model selection, they leverage the Azure CLI to deploy this model and environment to a LINUX VM in Azure.  This Azure VM will run as the scoring engine (Inference) for production applications or as an MVP app to monitor model performance.  The hardware profile for the inference instance will be different than the training instance.  The ML Engineer will need to right size the environment for the amount of traffic more than the size of the train/test data sets.

Here are the Azure Services that support AI & ML workloads
1.  Local Web Service (Docker Image)
2.	Remote VM (Azure VM, Kubernetes, AKS)
3.	Windows ML
 
The learning resources will not be a deep dive into how to support and develop in these environments.  The intent is how to deploy AI & ML into these compute environments.  The set of learning resources are curated to help you get to a level 300 understanding.


|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Local Web Service| 100|[How do you deploy a machine learning model as a web service within Azure?](https://youtu.be/n8h6_Expf38)|
|| 200|[Deploy a TensorFlow model served with TF Serving using a custom container in an online endpoint](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-deploy-custom-container?tabs=cli)|
|| 300 |[Register model and deploy locally](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/deployment/deploy-to-local/register-model-deploy-local.ipynb)|
| Remote VM| 100|[Model deployment and inferencing with Azure Machine Learning](https://www.youtube.com/watch?v=WZ7vS10KPAw&ab_channel=MicrosoftAzure)|
|| 200|[ONNX and Azure Machine Learning: Create and accelerate ML models](https://learn.microsoft.com/en-us/azure/machine-learning/concept-onnx)|
|| 300 |[Deploying a web service to Azure Kubernetes Service (AKS)](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/deployment/production-deploy-to-aks/production-deploy-to-aks.ipynb)|
| Windows ML| 100|[Windows AI](https://learn.microsoft.com/en-us/windows/ai/)|
|| 200|[Image Classification with ML.NET and Windows Machine Learning](https://learn.microsoft.com/en-us/windows/ai/windows-ml/tutorials/mlnet-intro)|
|| 300 |[Windows Machine Learning Samples](https://learn.microsoft.com/en-us/windows/ai/windows-ml/samples)|




## Hosted Environment
A hosted environment will utilize a common runtime environment in terms of OS, Languages, Frameworks and IDEs.  The hosted environment is set up and supported by Azure.  The most common environment will be setup to ensure versatility but reduce setup time for these users.  A typical user for this environment is a Data Scientist who might be experts in model development but needs to hand-off their code set to experts to deploy into production.  A great example is Azure ML Notebooks.

These environments will be setup with a preconfigured set of ML Frameworks, Languages, packages and tools.  This is to ensure setup time is minimal for end-users.  This environment is typically setup for a Data Scientist who wants to build machine learning models but not an expert on configuration and infrastructure.  A data scientist will train/test new models, conduct exploratory data analysis, or ad-hoc experiments.  The simplicity of the environment is a big benefit but the flexibility to build a multitude of models for highest accuracy might be restrained depending on the configuration of these environments.  It is highly recommended to review the configuration so you fully understand the options.

Here are the Azure Services that support AI & ML workloads
1.  DS VM
2.  Synapse Analytics Spark Pools
3.  Synapse Analytics Workspace
4.  Azure Machine Learning Notebooks
5.  Azure Machine Learning Attached Compute
5.  Azure Databricks
6.  HDInsight
 
The learning resources will not be a deep dive into how to support and develop in these environments.  The intent is how to deploy AI & ML into these compute environments.  The set of learning resources are curated to help you get to a level 300 understanding.


|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| DSVM| 100|[Data Science Virtual Machine Overview (DSVM)](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/overview)|
|| 200|[Data Science Tools on DSVM](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/tools-included)||
|| 300|[Samples on the DSVM](https://learn.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-samples-and-walkthroughs)||
| Synapse Analytics Workspace| 100|[Machine Learning Experiences in Azure Synapse](https://www.youtube.com/watch?v=xf3Lej-MWCk&ab_channel=MicrosoftDeveloper)|
|| 200|[Cognitive Services in Azure Synapse ANalytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/machine-learning/overview-cognitive-services)||
|| 300 |[Train ML model without code](https://learn.microsoft.com/en-us/azure/synapse-analytics/machine-learning/tutorial-automl)||
| Synapse Analytics Spark Pools| 100|[Synapse Analytics Spark Pools Overview](https://www.youtube.com/watch?v=SPOQzcbTgvQ&t=136s)||
|| 200|[Apache Spark MLLib running on Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/spark/apache-spark-machine-learning-mllib-notebook)||
|| 300 |[SynapseML running on Synapse Analytics Spark Pools](https://github.com/microsoft/SynapseML#synapse-analytics)||
| AML Notebooks| 100|[Azure Machine Learning Studio Notebooks](https://www.youtube.com/watch?v=AAj-Fz0uCNk&ab_channel=MicrosoftDeveloper)|
|| 200|[How to run Jupyter notebooks on AML](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-run-jupyter-notebooks)||
|| 300 |[Image Classification Using Notebooks in AML](https://www.youtube.com/watch?v=O5bePha5RiY&t=947s&ab_channel=MicrosoftDeveloper)||
| AML Compute| 100|[Learn how to utilize right compute for AML Training jobs](https://www.youtube.com/watch?v=_N8RXm2QrrM&ab_channel=MicrosoftAzure)|
|| 200|[What is an Azure Machine Learning Compute instance](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-instance)|
|| 300 |[AML Training Compute Targets](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-target#training-compute-targets)|
| Databricks| 100|[Azure Databricks Overview](https://learn.microsoft.com/en-us/azure/databricks/scenarios/what-is-azure-databricks-ml)|
|| 200|[Deploy models for inference and prediction](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/model-inference/)||
|| 300 |[Model training examples](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/train-model/)||


## Managed Environment
This environment is similar to a PaaS or SaaS Azure service where the developer isn't concerned with setup of their environment or availability of the service.  Their main concern is the scalability of the environment to service the traffic to score the data.  Managed environments start to transition from a Data Scientist to a more Low-code option to streamline adoption by Citizen Developers.  Managed environments are not typically leveraged by Pro-Developers since they like to Build their own thru a Software Development Lifecycle.

These environments are pre-built environments with varying degrees of model portability.  The purpose is to reduce machine learning model development/deployment time.  A software engineer might not have extensive data science skills but with Cognitive Services they can reuse prebuilt models to score their data for sentiment analysis.  Likewise, a database developer might want to run a batch inference script (T-SQL) to score the new data in the database platform.  Lastly, a data scientist who needs to wear multiple hats can leverage the Azure ML Service for an end-to-end for training and scoring their data.

Here are the Azure Services that support AI & ML workloads
1.  Applied AI
2.	Cognitive Services
3.	SQL Server Machine Learning Service
5.  Azure SQL Managed Instance
6.  AML Inference Cluster
7.  AML Attached Compute
8.  AML Managed Endpoints
10. Azure Batch
11.  SQL Edge
12.  IoT Edge

The learning resources will not be a deep dive into how to support and develop in these environments.  The intent is how to deploy AI & ML into these compute environments.  The set of learning resources are curated to help you get to a level 300 understanding.

|                              |                              |                              |
|------------------------------|------------------------------|------------------------------|
| **Resource**	| **Level** | **Training Assets URL**|
| Applied AI| 100|[Azure Applied AI Services Overview](https://www.youtube.com/watch?v=M6wxdYQrAnQ&ab_channel=MicrosoftDeveloper)|
|| 200|[Prebuilt AI models in customer applications](https://www.youtube.com/watch?v=45we8bNPsBc&ab_channel=MicrosoftDeveloper)|
|| 300 |[Form Recognizer Tutorial](https://learn.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/tutorial-logic-apps)|
| Cognitive Services| 100|[Getting Started with Cognitive Services](https://techcommunity.microsoft.com/t5/apps-on-azure-blog/integrating-ai-best-practices-and-resources-to-get-started-with/ba-p/2271522)|
|| 200|[Cognitive Services Development Option](https://learn.microsoft.com/en-us/azure/cognitive-services/cognitive-services-development-options)|
|| 300 |[Cognitive Services Containers](https://learn.microsoft.com/en-us/azure/cognitive-services/cognitive-services-container-support)|
| SQL Server ML Svc| 100|[SQL Server & Machine Learning Service Overview](https://learn.microsoft.com/en-us/sql/machine-learning/sql-server-machine-learning-services?view=sql-server-ver16)|
| Azure SQL Managed Instance| 100|[Machine Learning Services in Azure SQL Managed Instance](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/machine-learning-services-overview?view=azuresql)|
|| 200|[Key Differences in Managed Instance and SQL Server](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/machine-learning-services-differences?view=azuresql)|
|| 300 |[Linear Regression tutorial for Managed Instance](https://learn.microsoft.com/en-us/sql/machine-learning/tutorials/python-ski-rental-linear-regression?view=azuresqldb-mi-current)|
| AML Inference Compute| 100|[Model Deployment and Inferencing in AML](https://www.youtube.com/watch?v=WZ7vS10KPAw&ab_channel=MicrosoftAzure)|
|| 200|[Compute Targets for Inference](https://learn.microsoft.com/en-us/azure/machine-learning/concept-compute-target#compute-targets-for-inference)|
|| 300 |[Attach AKS to Azure ML Workspace](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-attach-kubernetes-to-workspace?source=recommendations&tabs=cli)|
| AML Managed Endpoint| 100|[AML Endpoint Overview](https://learn.microsoft.com/en-us/azure/machine-learning/concept-endpoints-online?view=azureml-api-2)|
|| 200|[Score model with online endpoint](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-deploy-managed-online-endpoints?tabs=azure-cli)|
|| 300 |[AML in a Day Tutorial](https://learn.microsoft.com/en-us/azure/machine-learning/tutorial-azure-ml-in-a-day)|
| SQL Edge| 100|[What is Azure SQL Edge](https://www.youtube.com/watch?v=QkuJs7S8e6w&ab_channel=MicrosoftDeveloper)|
|| 200 |[Machine Learning on the SQL Edge](https://learn.microsoft.com/en-us/azure/azure-sql-edge/onnx-overview)|
|| 300|[Deploy ONNX model TO SQL Edge](https://learn.microsoft.com/en-us/azure/azure-sql-edge/deploy-onnx)|
| IoT Edge| 100|[Audio on the Vision AI DevKit](https://learn.microsoft.com/en-us/shows/internet-of-things-show/use-audio-on-the-vision-ai-devkit)|
|| 200 |[Vision Developer Kit for Audio Processing](https://github.com/ksaye/vision-ai-developer-kit-audio/tree/master/documentation)|
|| 300|[End to End Tutorial for AML and IoT Edge](https://learn.microsoft.com/en-us/azure/iot-edge/tutorial-machine-learning-edge-01-intro?source=recommendations&view=iotedge-2018-06)|
