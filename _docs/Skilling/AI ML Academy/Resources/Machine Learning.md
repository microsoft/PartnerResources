---
layout: page
title: Machine Learning
description: Resources for Azure Machine Learning (AML)
updated: 2024-01-31
permalink: /skilling/ai-ml-academy/resources/machine-learning
tags:
- azure
- learning plan
- academy content
- aiml resources
---

# Machine Learning (ML) Resources

This learning plan will guide you through implementing Machine Learning (ML) solutions on Azure with Azure Machine Learning (AML), a suite of services that enables those new to ML, as well as experienced data scientists, to build and operate ML models.

To make AI accessible for all experience levels, Azure ML features a no-code Automated ML service, a low-code drag-and-drop Designer interface, and a full-featured Python SDK for code development within Jupyter Notebooks or your IDE of choice.

## Fundamentals

* [Microsoft Azure AI Fundamentals](https://learn.microsoft.com/en-us/training/paths/get-started-with-artificial-intelligence-on-azure/) – A good overview of fundamental concepts for AI and ML on Azure, along with an intro to Azure OpenAI
* [Azure Machine Learning Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/) – Documentation for Azure ML, covering concepts such as how to train, deploy, and manage your ML models
* [Introduction to Azure Machine Learning SDK V2 and CLI V2](https://www.youtube.com/watch?v=unbzStG3IVY&ab_channel=MicrosoftDeveloper) – Video describing the new V2 version of Azure ML, its features, and capabilities, along with a demo
* [Automated Machine Learning Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-automated-ml) – All about Azure ML's Automated ML service that enables no-code ML model training and deployment
    * [Automated Machine Learning on Azure (Video)](https://www.youtube.com/watch?v=tXrDscVaF4Q&ab_channel=MicrosoftDeveloper) – Video describing what's new in Automated ML in V2 with a demo
    * [Use Automated Machine Learning in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/use-automated-machine-learning/) – A step-by-step tutorial on how to use Auto ML in Azure ML
* [Designer Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/concept-designer) – All about Azure ML’s drag-and-drop Designer and its capabilities
    * [Low-code Machine Learning in Azure – Machine Learning Essentials](https://www.youtube.com/watch?v=mwJ5Vbmy1AM) – A visual to demonstrate ML Designer
    * [Explore visual tools for Machine Learning on Azure ML](https://learn.microsoft.com/en-us/training/paths/create-no-code-predictive-models-azure-machine-learning/) – A step-by-step tutorial on creating a classification, regression, and clustering model within ML Designer

## Associate

* [Python SDK Documentation](https://docs.microsoft.com/en-us/python/api/overview/azure/ml/?view=azure-ml-py) – A good overview of the Azure ML SDK and its features
    * [Tutorial: Get started creating your first ML experiment with the Python SDK](https://docs.microsoft.com/en-us/azure/machine-learning/service/tutorial-1st-experiment-sdk-setup)
        * Part 1 – Create a compute instance using Azure ML
        * Part 2 – Train a model: Follow the Next Steps on the bottom of Part 1 to train your image classification model with MNIST data and scikit-learn 
        * Part 3 – Deploy a model: Follow the Next Steps on the bottom of Part 2 to deploy the classification model in Azure Container Instances  
* [Azure Machine Learning Exercises SDK v2](https://microsoftlearning.github.io/mslearn-azure-ml/) – A repository of hands-on lab exercises that support DP-100. Consists mainly of notebooks and tutorials on how to use the Azure ML SDK
* [How to use Azure Machine Learning SDK v2](https://github.com/Azure/azureml-examples) - A GitHub repository filled with hands-on practice for experimentation and model management
* [Working with Compute Contexts in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/use-compute-contexts-in-aml/) – A guide with information on environments and compute contexts as well as hands-on practice
* [Working with Data in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/work-with-data-in-aml/) – A repository of information regarding datasets and datastores in Azure ML
* [Deploy real-time Machine Learning services with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/register-and-deploy-model-with-amls/?OCID=AID3027817) – A tutorial on how to register and deploy ML models using Azure ML

## Expert

* [Orchestrating Machine Learning with pipelines](https://docs.microsoft.com/en-us/learn/modules/create-pipelines-in-aml/) – Learn to create, publish, and run Azure ML pipelines
* [Deploy batch inference pipelines with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/deploy-batch-inference-pipelines-with-azure-machine-learning/) – Learn to create, deploy, and use batch inference pipelines
* [Explain Machine Learning models with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/explain-machine-learning-models-with-azure-machine-learning/?OCID=AID3027817) – Learn to explain models by calculating and interpreting feature importance
* [Tune hyperparameters with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/tune-hyperparameters-with-azure-machine-learning/?OCID=AID3027817) – Tutorial on hyperparameter sweeping to optimize your ML models
* [Monitor models with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/monitor-models-with-azure-machine-learning/?OCID=AID3027817) – Learn to run hyperparameter tuning experiments to optimize ML model performance
* [Monitor data drift with Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/monitor-data-drift-with-azure-machine-learning/?OCID=AID3027817) – Learn to configure data drift monitoring to detect changes in data over time
* [MLOps Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/concept-model-management-and-deployment) – Documentation on Azure ML Operations (MLOps) for building efficient ML workflows, including continuous integration, delivery, and deployment (CI/CD)

## Specialist
* [Recommendation System Best Practices & GitHub Examples](https://github.com/microsoft/recommenders) – GitHub repository containing examples and best practice guidelines for recommendation systems
* [Computer Vision Best Practices & GitHub Samples](https://github.com/microsoft/computervision-recipes?OCID=AID3027817) – GitHub repository containing examples and best practice guidelines for Computer Vision systems
* [Azure Machine Learning Security](https://github.com/jhirono/amlsecurity) – A repository of information on how to provision secure workplaces in Azure ML

 
## Certifications

DP-100 applies your knowledge of data science and ML to implement and run ML workloads on Azure; in particular, using Azure ML. This is the most ML-heavy certification.

* [DP-100](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-100)

You may also consider taking AI-102 to skill up on Azure AI services, ML, and knowledge mining or DP-203 to skill up on the data engineering portion of an ML project.

* [AI-102](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-102/)
* [DP-203](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-203/)