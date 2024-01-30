---
layout: page
title: Machine Learning
description: Resources for Azure Machine Learning (ML)
updated: 2024-01-29
permalink: /azure/data-analytics-ai/machine-learning
tags: 
- azure
- data, analytics, and ai
- learning plan
- machine learning
- ai
---

# Machine Learning Readiness Resources

This learning plan will guide you through implementing Machine Learning (ML) solutions on Azure with Azure Machine Learning, a suite of services that enables those new to ML, as well as experienced data scientists, to build and operationalize ML models.   

To make AI accessible for all experience levels, Azure ML features a no-code Automated ML service, a low-code drag-and-drop Designer interface, and a full-featured Python SDK for code development within Jupyter Notebooks or your IDE of choice. 


## Fundamentals

* [Microsoft Azure AI Fundamentals](https://learn.microsoft.com/en-us/training/paths/get-started-with-artificial-intelligence-on-azure/) (Self-Paced) – A good overview of fundamental concepts for AI and ML on Azure, along with an intro to Azure Open AI
* [Azure Machine Learning Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/) (Self-Paced) - Documentation for Azure Machine Learning, covering concepts such as how to train, deploy, and manage your machine learning models
* [Introduction to Azure ML SDK V2 and CLI V2](https://www.youtube.com/watch?v=unbzStG3IVY&ab_channel=MicrosoftDeveloper)) (Self-Paced) - Video describing the new V2 version of Azure ML, its features and capabilities along with a demo.
* [Automated ML Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-automated-ml) (Self-Paced) – All about Azure Machine Learning’s Automated ML service that enables no-code ML model training and deployment 
    * [Automated Machine Learning on Azure (Video)](https://www.youtube.com/watch?v=tXrDscVaF4Q&ab_channel=MicrosoftDeveloper)(20 minutes) - Video describing what's new in Automated ML in V2 with a demo.   
    * [Use automated machine learning in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/use-automated-machine-learning/) (Self-Paced) (39 Minutes) - A step by step tutorial on how to use Auto ML in Azure Machine Learning. 
* [Designer Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/concept-designer) - All about Azure Machine Learning’s drag-and-drop Designer and its capabilities. 
    * [Low-code machine learning in Azure | Machine Learning Essentials](https://www.youtube.com/watch?v=mwJ5Vbmy1AM) (Video) (11 Minutes) - A visual to demonstrate Machine Learning designer. 
    * [Explore visual tools for Machine Learning on Azure ML](https://learn.microsoft.com/en-us/training/paths/create-no-code-predictive-models-azure-machine-learning/) (Self-Paced) (4 hours) - A step by step tutorial on creating a classification, regression and clustering model within ML designer. 
* [Machine Learning Tech Talk](https://msuspartners.eventbuilder.com/event/39234?source=AzurePartnerTechTalks) (Recorded Webinar) (58 Minutes) - Simplifying ML Lifecycle for All Data Personas
* [Machine Learning Tech Talk](https://msuspartners.eventbuilder.com/event/21258?source=AzurePartnerTechTalks) (Recorded Webinar) (1 Hour 29 Minutes) Responsible AI/ML for Model Developers

## Associate

* [Python SDK Documentation](https://docs.microsoft.com/en-us/python/api/overview/azure/ml/?view=azure-ml-py) (Self-Paced) - A good overview of the Azure Machine Learning SDK and its features. 
    * [Tutorial: Get started creating your first ML experiment with the Python SDK](https://docs.microsoft.com/en-us/azure/machine-learning/service/tutorial-1st-experiment-sdk-setup) (Self-Paced) (2 Hours) –  
        * Part 1 – Create a compute instance using Azure Machine Learning  
        * Part 2 – Train a model: Follow the Next Steps on the bottom of Part 1 to train your image classification model with MNIST data and scikit-learn 
        * Part 3 – Deploy a model: Follow the Next Steps on the bottom of Part 2 to deploy the classification model in Azure Container Instances  
* [Microsoft Learn - Azure Machine Learning Exercises SDK v2](https://microsoftlearning.github.io/mslearn-azure-ml/) (Self-paced) (8 Hours) - A repository of hands-on lab exercises that support DP-100. Consists mainly of notebooks and tutorials on how to use the AML SDK.     
* [How to use Azure ML SDK v2](https://github.com/Azure/azureml-examples) - A GitHub repository filled with hands-on practice for experimentation and model management.
* [Working with Compute Contexts in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/use-compute-contexts-in-aml/) (Self-Paced) (47 Minutes) - A guide with information on environments and compute contexts as well as hands-on practice. 
* [Working with Data in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/work-with-data-in-aml/) (Self-Paced) (47 Minutes) - A repository of information regarding datasets and datastores in Azure Machine Learning. 
* [Deploy real-time machine learning services with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/register-and-deploy-model-with-amls/?OCID=AID3027817) (Self-Paced) (40 Minutes) - A tutorial on how to register and deploy ML models using Azure ML. 

## Expert

* [Orchestrating machine learning with pipelines](https://docs.microsoft.com/en-us/learn/modules/create-pipelines-in-aml/) (Self-Paced) (57 Minutes) – Learn to create, publish, and run Azure Machine Learning pipelines 
* [Deploy batch inference pipelines with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/deploy-batch-inference-pipelines-with-azure-machine-learning/) (Self-Paced) (44 Minutes) – Learn to create, deploy, and use batch inference pipelines 
* [Explain machine learning models with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/explain-machine-learning-models-with-azure-machine-learning/?OCID=AID3027817) (Self-Paced) (47 Minutes) – Learn to explain models by calculating and interpreting feature importance. 
* [Tune hyperparameters with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/tune-hyperparameters-with-azure-machine-learning/?OCID=AID3027817) (Self-Paced) (46 Minutes) – Microsoft Learn tutorial on hyperparameter sweeping to optimize your ML models 
* [Monitor models with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/monitor-models-with-azure-machine-learning/?OCID=AID3027817) (Self-Paced) (39 Minutes) – Learn to run hyperparameter tuning experiments to optimize model performance 
* [Monitor data drift with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/monitor-data-drift-with-azure-machine-learning/?OCID=AID3027817) (Self-Paced) (42 Minutes) – Learn to configure data drift monitoring to detect changes in data over time 
* [MLOps Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/concept-model-management-and-deployment) (Self-Paced) – Documentation on Azure Machine Learning Operations (MLOps) for building efficient ML workflows, including continuous integration, delivery, and deployment 
    * [MLOPS What The Hack](https://github.com/ShivaKumarChittamuru/WhatTheHack/tree/master/032-MLOpsFromScratch) (Self-Paced) – GitHub repository containing a challenge-based hackathon on MLOps.  You are presented with challenges to work through and solve as you learn MLOps concepts and practices. 


## Specialist
* [Recommendation System Best Practices & Github Examples](https://github.com/microsoft/recommenders) (Self-Paced) (8 Hours) - Github repository containing examples and best practice guidelines for recommendation systems. 
* [NLP Best Practices & Github Examples](https://github.com/microsoft/nlp-recipes?OCID=AID3027817) (Self-Paced) (8 Hours) - Github repository containing examples and best practice guidelines for Natural Language Processing Systems. 
* [Computer Vision Best Practices & GitHub Samples](https://github.com/microsoft/computervision-recipes?OCID=AID3027817) (Self-Paced) (8 Hours) - Github repository containing examples and best practice guidelines for Computer Vision Systems. 
* [Azure ML Security](https://github.com/jhirono/amlsecurity) (Self-Paced) (4 Hours) - A repository of information on how to provision secure workplace in Azure Machine Learning.  

 
## Certifications

DP-100 applies your knowledge of data science and machine learning to implement and run machine learning workloads on Azure; in particular, using Azure Machine Learning Service. This is the most Machine Learning heavy certification. 

* [DP-100](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-100)

You may also consider taking AI-102 to skill up on Azure ai services, machine learning, and knowledge mining or DP-203 to skill up on the data engineering portion of a machine learning project. 

* [AI-102](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-102/)
* [DP-203](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-203/)

