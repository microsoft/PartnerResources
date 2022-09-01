---
layout: page
title: AI & ML Academy - Azure ML
description: Workshop focused on AI and ML - Azure ML
permalink: /skilling/ai-ml-academy/azure-ml
updated: 2022-09-01
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- workshop
---

# Azure Machine Learning

## What is Azure Machine Learning (AML)?
Azure Machine Learning (AML) is a cloud service for accelerating and managing the machine learning project lifecycle. 
Machine learning professionals, data scientists, ML engineers can use it in their day-to-day workflows: 
- Experimentation,
- Model training,
- Model deployment,
- MLOps.

AML is for individuals and teams implementing MLOps within their organization to bring machine learning models into production in a secure and auditable production environment. [What is Azure Machine Learning? - Azure Machine Learning | Microsoft Docs](https://docs.microsoft.com/en-us/azure/machine-learning/overview-what-is-azure-machine-learning).


To understand how AML helps users, let's compare two cases of implementing an end-to-end ML project without and with AML.

### Without Azure ML
1. Computer. This is usually our laptop with limited capacity.

2. Python environment. Best practice is to create a virtual environment per project, and install all necessary packages. It takes some time and configuring some packages with each other (e.g., tensorflow, pytorch) may be difficult. Some packages may not work on some operating systems. 

3. Data. During the development, we usually use CSV sample files. Sometimes, we need to reconfigure the code to accept data in a different format in production.

4. Modeling. During modeling, we experiment with different parameters and models. In each experiment, we may change some of the previous parameters. We usually lose track of the parameters after a couple of iterations. 

5. Deployment. Once our model is developed, we store it as a file (`pkl`, `json`, etc.) and create a container. This requires creating or re-using a `dockerfile` and customizing it to fit our usecase. Once the image is built, we push it to a container repository and deploy it on a cluster (kubernetes, On-prem, Azure, other clouds).

### With Azure ML
1. You create a compute instance, which belongs to you only. It can have as much CPU, GPU, memory as you need. If you have for example two usecases, where first one requires a high-end and expensive setting and the second one requires only a low-end config, you can provision two compute instances. You will be charged only for the amount of time each machine is on.

2. Python environment. Azure provides out-of-the-box many curated environments that cover majority of usecases. All dependencies are pre-installed. In the unlikely event that none of them serve your need, you can use the terminal of your compute instance and create your own environment. 

3. Data. AML introduces concept of datasets. A dataset is an abstraction of data. It can be tabular data or file data (e.g., images, audio files, ...). A tabular dataset can be constructed from a local CSV file. However, with AML you have many more efficient options such as executing a SQL query against an Azure SQL database, Azure MySQL database, Azure PostgreSQL, or reading CSV or parquet from Azure Storage or ADLS gen 2. You can also read from web files. File datasets can be uploaded locally or connect to Azure Storage or ADLS  gen 2. Since AML datasets act as an interface, your code does not need to change whe nyou switch from a sample csv file to a large cloud-hosted file or SQL query in production. 

4. Modeling. AML introduces experiment and model abstractions similar to Datasets. An experiment keeps track of all of the code changes, input parameters, output metrics (accuracy, percision, recall, ), and custom parameters and metrics unique to your usecase.
AML experiments dashboard shows you all of your experiments and their associated information as well as the model files. So, when you find the best model, you don't need to run it again to generate the binaries. This is achieved through AML Model abstraction. 

5. Once your model is ready in AML, you can either use the AML GUI to deploy your model as an endpoint or deploy it in your python notebook with less than 10 lines of code. AML containerizes your model, scoring script, and required packages. It then deploys it to your desired destination (Kubernetes, Azure Container Instance, ...). And generates a URL so you can call it. You can use default configs or customize as much as you need.

Check out these repositories for examples of development and deployment on AML.

(https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml)

(https://github.com/microsoft/solution-accelerator-many-models)

(https://github.com/Azure/azureml-examples)

#### Bonus features of AML
There are some bonus features in AML that you don't have with traditional ML lifecycle.
1. AutoML. AutoML is a smart tool that accepts a dataset (tabular or file) and produces your desired model. It can perform classification, clustering, regression tasks on datasets. AutoML tries tens or even hundreds of models from the literature, performs data cleaning, normalization, preprocessing, and trains all of them. It then reports to you the metrics for all of the calculated model, with recommendations. You can choose which model(s) to deploy with one click.
[Use automated machine learning in Azure Machine Learning - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/use-automated-machine-learning/)

2. Designer. 
[Create a regression model with Azure Machine Learning designer - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/create-regression-model-azure-machine-learning-designer/)

3. Pipelines.
[Orchestrate machine learning with pipelines - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/create-pipelines-in-aml/)

4. Responsible AI

5. ...


