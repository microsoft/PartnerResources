---
layout: page
title: AI & ML Academy - Build Your Own ML
sorttitle: 04
description: Build Your Own ML
permalink: /skilling/ai-ml-academy/build-your-own-ml
updated: 2024-04-22
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- academy content
- ai & ml academy module
- ai & ml academy
- build your own ml
---

# AI & ML Academy - Build Your Own ML

Welcome to the AI & ML Academy (AIA) - Build Your Own ML!

## What is Azure Machine Learning?
Azure Machine Learning (Azure ML, or AML) is a cloud service for accelerating and managing the machine learning project lifecycle. 
Machine learning professionals, data scientists, and ML engineers can use it in their day-to-day workflows for:

- Experimentation,
- Model training,
- Model deployment,
- MLOps.


## Who is Azure ML for?
Azure ML is for individuals and teams implementing MLOps within their organization to bring machine learning models into production in a secure and auditable production environment. With AML:

1. **Data scientists** and **ML engineers** will find tools to accelerate and automate their day-to-day workflows. 
2. **Application developers** will find tools for integrating models into applications or services. 
3. **Platform developers** will find a robust set of tools, backed by durable Azure Resource Manager APIs, for building advanced ML tooling. 
4. **Enterprises** working in the Microsoft Azure cloud will find familiar security and role-based access controls (RBAC) for infrastructure. You can set up the security to deny access to protected data and select operations.

Machine learning projects often require a team with varied skillsets to build and maintain. Azure ML has tools that help enable collaboration, such as:

1. Shared notebooks, compute resources, data, and environments
2. Tracking and auditability of experiments, models, and datasets
3. Built-in asset versioning and git integration for code versioning


## Why Azure ML?
To understand how Azure ML helps users, let's compare two cases of implementing an end-to-end ML project without and with Azure ML.

### Without Azure ML
1. **Computer.** This is usually your laptop with limited capacity.

2. **Python environment.** Best practice is to create a virtual environment per project and install all necessary packages. It takes some time and configuring some packages with each other (e.g., tensorflow, pytorch) may be difficult. Some packages may not work on some operating systems. 

3. **Data.** During the development, we usually use CSV sample files. Sometimes, we need to reconfigure the code to accept data in a different format in production.

4. **Modeling.** During modeling, we experiment with different parameters and models. In each experiment, we may change some of the previous parameters. We usually lose track of the parameters after several iterations. 

5. **Deployment.** Once your model is developed, we store it as a file (`pkl`, `json`, etc.) and create a container. This requires creating or re-using a `dockerfile` and customizing it to fit your use case. Once the image is built, we push it to a container repository and deploy it on a cluster (Kubernetes, On-prem, Azure, other clouds).

### With Azure ML
1. You create a compute instance, which belongs to you only. It can have as much CPU, GPU, memory as you need. If you have for example two use cases, where the first one requires a high-end and expensive setting and the second one requires only a low-end config, you can provision two compute instances. You will be charged only for the amount of time each machine is on. Azure ML also provides compute clusters, consisting of a pool of compute nodes that automatically scale up and down to speed up your compute-heavy tasks. You can, for example, develop your notebook and prepare the data on your compute instance, and then submit your training as a job to a compute cluster. Clusters can be set to automatically turn off if there are no jobs. 
    - To create a compute resource from GUI, in your Azure ML workspace, select __Compute__ from the left sidebar. Conveniently, create a __Compute instance__, __Compute cluster__, or __Attached cluster__ by following the prompts.
    - To create a compute resource using Azure ML Python SDK, you can use the sample code below. You may need to create a compute resource using Python code in the following situations: 1) in automated ML pipelines it is preferred to create resources and then dispose of them, your code can perform all in one file; 2) automated resource provisioning, more suitable for administration, to ensure resources are generated with standard configurations across the enterprise.

    ```py
    from azureml.core import Workspace 
    from azureml.core.compute import ComputeTarget, ComputeInstance
    from azureml.core.compute_target import ComputeTargetException

    ws = Workspace.from_config() # there are multiple ways to obtain the workspace object, this is for example only

    def create_or_get_aml_compute_instance(ws: Workspace, compute_name: str, *, vm_size='STANDARD_D3_V2', ):
        ''' Tries to get the compute node, if it does not exist, creates one based on the provided vm_size.'''
        try:
            instance = ComputeInstance(workspace=ws, name=compute_name)
            print('Found existing instance, use it.')
        except ComputeTargetException:
            compute_config = ComputeInstance.provisioning_configuration(
                vm_size=vm_size,
                ssh_public_access=False,
                # vnet_resourcegroup_name='<my-resource-group>',
                # vnet_name='<my-vnet-name>',
                # subnet_name='default',
                # admin_user_ssh_public_key='<my-sshkey>'
            )
            instance = ComputeInstance.create(ws, compute_name, compute_config)
            instance.wait_for_completion(show_output=True)
        finally:
            return instance

    def create_or_get_aml_compute_cluster(ws: Workspace, cluster_name: str, *, vm_size='STANDARD_D3_V2', max_nodes=4, ):
        ''' Tries to get the compute cluster, if it does not exist, creates one based on the provided kwargs.'''    
        try:
            cpu_cluster = ComputeTarget(workspace=ws, name=cluster_name)
            print('Found existing cluster, use it.')
        except ComputeTargetException:
            # To use a different region for the compute, add a location='<region>' parameter
            compute_config = AmlCompute.provisioning_configuration(vm_size=vm_size,
                                                            max_nodes=max_nodes)
            cpu_cluster = ComputeTarget.create(ws, cluster_name, compute_config)
            cpu_cluster.wait_for_completion(show_output=True)
        finally: 
            return cpu_cluster

    ```

    For more info and examples visit **[this page](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-manage-compute-instance?tabs=python).**

2. Python environment. Azure provides out-of-the-box curated environments that cover a majority of use cases. All dependencies are pre-installed. In the unlikely event that none of the environments serve your needs, you can use the terminal of your compute instance to create your own environment.

    To standardize the environment across users and compute resources, Azure ML also provides its own abstraction of Environment. There are dozens of curated environments pre-built by Microsoft to speed up your ML work. You can create your own environment by starting from scratch (e.g., a docker file) or extend an existing environment to customize to your needs.

    Explore **[this article](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-manage-environments-in-studio)** or **[this doc](https://docs.microsoft.com/en-us/python/api/azureml-core/azureml.core.environment.environment?view=azure-ml-py)** for more information.
  <!-- ```py
  ```  -->

3. Data. Azure ML introduces concept of datasets. A dataset is an abstraction of data. It can be tabular data or file data (e.g., images, audio files, ...). A tabular dataset can be constructed from a local CSV file. However, with Azure ML, you have many more efficient options, such as executing an SQL query against an Azure SQL database, Azure MySQL database, Azure PostgreSQL, or reading CSV or parquet from Azure Storage or ADLS gen 2. You can also read from web files. File datasets can be uploaded locally or connected to Azure Storage. Since Azure ML datasets act as an interface, your code does not need to change when you switch from a sample csv file to a large cloud-hosted file or SQL query in production.
    ```py
    from azureml.core import Workspace, Dataset

    def get_dataset_by_name(ws: Workspace, dataset_name: str, version='latest'):
        dataset_object = Dataset.get_by_name(ws, dataset_name, version)
        df = dataset_object.to_pandas_dataframe() # if you need a pandas df
        df = dataset_object.to_dask_dataframe()   # if you need a dask df
        df = dataset_object.to_spark_dataframe()  # if you need a spark df, requires spark to be installed in your env
        return df 

    ```

    Closely related to Datasets in Azure ML are _Datastores_. While Dataset is an interface to the data, Datastore is the interface to the  physical location of the data. For example, to access files in an Azure Data Lake (ADLS), you must first create a Datastore that provides the required connection parameters. You can then use this datastore to create datasets that read data from this storage account. By default, Azure ML creates `workspaceblobstore` and `workspacefilestore` that link to the Storage account that was created with this Azure ML workspace. 

4. Modeling. Azure ML introduces experiment and model abstractions similar to Datasets. An experiment keeps track of all of the code changes, input parameters, output metrics (e.g., accuracy, precision, recall), and custom parameters and metrics unique to your use case. Azure ML experiments dashboard shows you all of your experiments and their associated information as well as the model files. So, when you find the best model, you won't need to run it again to generate the binaries. This is achieved through AML Model abstraction.

    ```py
    # Here is an example of using Logistic Regression in a classification project, evaluating, and registering the model
    from azureml.core import Workspace, Experiment, Model, Run, Dataset

    import joblib
    import os
    from sklearn.linear_model import LogisticRegression
    from sklearn.metrics import roc_auc_score

    # example of registering model inside an experiment 
    def perform_training_experiment(ws: Workspace, *,  
                                    X_train, X_test, y_train, y_test, reg: float, 
                                    experiment_name:str, artifacts_path: str, model_name: str,):
        # Create an Azure ML experiment in your workspace
        experiment = Experiment(ws, name= experiment_name)
        # an experiment manages the different runs
        run = experiment.start_logging() 
        run.log('Regularization Rate',  np.float(reg))
        model = LogisticRegression(C=1/reg, solver="liblinear").fit(X_train, y_train)

        # calculate accuracy and AUC
        y_hat = model.predict(X_test)
        y_scores = model.predict_proba(X_test)
        acc = np.average(y_hat == y_test)
        auc = roc_auc_score(y_test,y_scores[:,1])
        run.log('Accuracy', np.float(acc))
        run.log('AUC', np.float(auc))

        # save artifacts before finishing the run
        os.makedirs(artifacts_path, exist_ok=True) 
        model_filename = f'{artifacts_path}/{model_name}.pkl'
        joblib.dump(value=model, filename=model_filename)

        run.complete() # finish this run, run.logs will no longer record.
    
        run.register_model(model_path=model_filename, model_name=model_name,
            tags={'Model Type':'Logistic Regresssion', 'Other':'tags'})

    # now perform several experiment runs with different parameters  
    perform_training_experiment(ws, reg=0.01, ...)
    perform_training_experiment(ws, reg=0.02, ...)
    perform_training_experiment(ws, reg=0.03, ...)

    # Visit Azure ML Experiments tab to see your experiment. 
    # Click on it and you will see 3 runs corresponding to the above 3 runs.
    # You can see the regularization rate of each experiment and the resulting 
    # Accuracy and AUC. 
    # Also, you can find the trained model in each run by clicking on the run and going to Artifacts tab.
    ```

5. Once your model is ready in Azure ML, you can either use the AML GUI to deploy your model as an endpoint or deploy it in your Python notebook with less than 10 lines of code. Azure ML containerizes your model, scoring script, and required packages. It then deploys it to your desired destination (Kubernetes, Azure Container Instance, ...). And generates a URL so you can call it. You can use default configs or customize needed.

    To deploy a model, you need the following:
    a) a Python file that explains how your model must be used for scoring. It is commonly named `score.py`. It must contain a function `init()` and another `run(payload)`. `init` is called once when the API server starts up. `run` is called every time a request comes to your API. Request payload is passed to your `run` function. Here is an example of a `score.py` file.

    ```py
    # score.py
    import os
    import joblib 

    def init():
        global model
        model_dir = os.getenv('AZUREML_MODEL_DIR') # Azure ML copies your registered model automatically to this folder
        model_path = os.path.join(model_dir, '<your model pkl file>.pkl')
        model = joblib.load(model_path) # make sure the related libraries are imported before (e.g., pandas, numpy, sklearn.linear_model.LogisticRegression)
    
    import json 
    def run(payload):
        data = json.loads(payload)
        X = transform(data) # You decide the form of the payload and how to convert it to acceptable form for your model
        y_pred = model.predict(X)
        return y_pred # Return the results. You can customize formatting (e.g., to a comparable format to input) for ease-of-use.
    
    def transform(data):
        # Optional function 
        # Perform data transformations needed to convert the input payload to a form acceptable for your model.
        # e.g., Convert JSON to pandas df or numpy array of arrays.
        # Raise exception if the input format does not match your intended format. 
        return data
    ```
    b) An environment in which your `score.py` file must be executed.
        
    ```py
    from azureml.core import Environment

    # example 1 env from conda yml file
    env = Environment.from_conda_specification(env_name, yml_file_path)
    env.python.user_managed_dependencies = False 

    # example 2 env from pip and requirements.txt
    env = Environment.from_pip_requirements(env_name, req_file_path)
    env.python.user_managed_dependencies = False 
    
    # example 3 env from dockerfile
    env = Environment(env_name)
    env.docker.base_image = None
    env.docker.base_dockerfile = "./my.dockerfile"
    env.python.user_managed_dependencies = True
    env.inferencing_stack_version = 'latest'
    env.python.interpreter_path = "/azureml-envs/myenv/bin/python"
    # to pass environment variables to your score.py file (in addition to the ones Azure ML passes automatically)
    # e.g., a service principal credentials, if you need to access other azure resources. 
    env.environment_variables = {
        "AZURE_CLIENT_ID": "PROVIDE YOUR  SERVICE PRINCIPLE CLIENT ID HERE",
        "AZURE_TENANT_ID": "PROVIDE YOUR SERVICE PRINCIPLE TENANT ID HERE",
        "AZURE_CLIENT_SECRET": "PROVIDE YOUR SERVICE PRINCIPLE CLIENT SECRET HERE",
    }
    ```

    Example accompanying `my.dockerfile`.
        
    ```Dockerfile
    FROM mcr.microsoft.com/azureml/openmpi3.1.2-ubuntu18.04:20210615.v1

    ENV AZUREML_CONDA_ENVIRONMENT_PATH /azureml-envs/myenv
    RUN conda create -p $AZUREML_CONDA_ENVIRONMENT_PATH python=3.8 pip=20.2.4
    ENV PATH $AZUREML_CONDA_ENVIRONMENT_PATH/bin:$PATH

    RUN apt-get install -y gcc

    RUN pip install \
        'joblib===1.1.0' \
        'pandas>=1.0' \
        'other packages here...'
    ```
    c) An Inference Config that ties your `score.py` to your `Environment` object.
    ```py
    from azureml.core.model import InferenceConfig
    inference_config = InferenceConfig(source_directory=score_py_folder, entry_script='score.py', environment=env)
    ```
    d) A deployment config. 
    ```py
    # if deploying to an Azure Container Instance (ACI), specify # of CPU cores, RAM, ... in the config
    from azureml.core.webservice import AciWebservice
    deployment_config = AciWebservice.deploy_configuration(cpu_cores=1, memory_gb=1, enable_app_insights=True)

    # if deploying to an Azure Kubernetes Service (AKS)
    from azureml.core.webservice import AksWebservice
    deployment_config = AksWebservice.deploy_configuration()

    # if deploying locally (only for test and debug)
    from azureml.core.webservice import LocalWebservice
    deployment_config = LocalWebservice.deploy_configuration(port=6789)
    ```
    e) Deploy!
    ```py
    from azureml.core import Model 
    
    my_model = Model(ws, name='my-model-name')

    my_service = Model.deploy(workspace=ws,
                    name=service_name,
                    models=[my_model], # must be a list, you can pass multiple models 
                    inference_config=inference_config,
                    deployment_config=deployment_config,
                    # deployment_target=aks_target, # if deploying to an AKS cluster
                )
    my_service.wait_for_deployment(show_output=True)

    # To find the my_service object later:
    my_service = ws.webservices[service_name]
    ```

Explore these repositories for examples of development and deployment on Azure ML:

- [Azure ML Notebooks](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml)
- [Azure ML Examples](https://github.com/Azure/azureml-examples)

#### Supportive features of AML
There are additional benefits with Azure ML that you may not have in traditional ML lifecycles.
1. __AutoML:__
    AutoML is a smart tool that accepts a dataset (tabular or file) and produces your desired model. It can perform classification, clustering, and regression tasks on datasets. AutoML tries tens or even hundreds of models from the literature, performs data cleaning, normalization, preprocessing, and trains all of them. It then reports to you the metrics for all of the calculated models, with recommendations. You can choose which model(s) to deploy with one click.
**[Use automated machine learning in Azure Machine Learning](https://docs.microsoft.com/en-us/learn/modules/use-automated-machine-learning/)**

2. __Designer__ and __Pipelines:__
    Azure ML designer is a low-code/no-code drag-and-drop interface used to train and deploy models in Azure ML. Use a visual canvas to build an end-to-end machine learning workflow. Train, test, and deploy models all in the designer:
    - Drag-and-drop data assets and components onto the canvas.
    - Connect the components to create a pipeline draft.
    - Submit a pipeline run using the compute resources in your Azure ML workspace.
    - Convert your training pipelines to inference pipelines.
    - Publish your pipelines to a REST pipeline endpoint to submit a new pipeline that runs with different parameters and data.
    - Publish a training pipeline to reuse a single pipeline to train multiple models while changing parameters and data.
    - Publish a batch inference pipeline to make predictions on new data by using a previously trained model.
    - Deploy a real-time inference pipeline to an online endpoint to make predictions on new data in real-time.

    A pipeline consists of data assets and analytical components, which you connect. Pipelines have many uses: you can make a pipeline that trains a single model, or one that trains multiple models. You can create a pipeline that makes predictions in real-time or in batch, and/or make a pipeline that only cleans data. Pipelines let you reuse your work and organize your projects.

    As you edit a pipeline in the designer, your progress is saved as a pipeline draft. You can edit a pipeline draft at any point by adding or removing components, configuring compute targets, creating parameters, and so on. Each time you run a pipeline, the configuration of the pipeline and its results are stored in your workspace as a pipeline job. You can go back to any pipeline job to inspect it for troubleshooting or auditing. Clone a pipeline job to create a new pipeline draft for you to edit. 


    **[Create a regression model with Azure Machine Learning designer](https://docs.microsoft.com/en-us/learn/modules/create-regression-model-azure-machine-learning-designer/)**
    
    **[Orchestrate machine learning with pipelines](https://docs.microsoft.com/en-us/learn/modules/create-pipelines-in-aml/)**

3. __Responsible AI:__
    Responsible Artificial Intelligence (Responsible AI) is an approach to developing, assessing, and deploying AI systems in a safe, trustworthy, and ethical way. From purpose to how people interact with AI systems, Responsible AI can help proactively guide these decisions toward more beneficial and equitable outcomes. Microsoft has developed a Responsible AI Standard. It's a framework for building AI systems according to six principles: fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability.

    **[Discuss practices for responsible AI at Microsoft](https://docs.microsoft.com/en-us/learn/modules/microsoft-responsible-ai-practices/)**
