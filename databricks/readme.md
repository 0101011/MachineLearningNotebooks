# Azure Databricks - Azure ML SDK Sample Notebooks

**NOTE**: With the latest version of our AML SDK, there are some API changes due to which previous version of notebooks will not work.
Kindly use this v4 notebooks (updated Sep 18)– if you had installed the AML SDK in your Databricks cluster please update to latest SDK version by installing azureml-sdk[databricks] as a library from GUI. 

**NOTE**: Please create your Azure Databricks cluster as v4.x (high concurrency preferred) with **Python 3** (dropdown). We are extending it to more runtimes asap.

**NOTE**: Some packages like psutil upgrade libs that can cause a conflict, please install such packages by freezing lib version. Eg. "pstuil **cryptography==1.5 pyopenssl==16.0.0 ipython=2.2.0**" to avoid install error. This issue is related to Databricks and not related to AML SDK.

**NOTE**: You should at least have contributor access to your Azure subcription to run some of the notebooks.

The iPython Notebooks have to be run sequentially after making changes based on your subscription. The corresponding DBC archive contains all the notebooks and can be imported into your Databricks workspace. You can the run notebooks after importing .dbc instead of downloading individually.  

This set of notebooks are related to Income prediction experiment based on this [dataset](https://archive.ics.uci.edu/ml/datasets/adult) and demonstrate how to data prep, train and operationalize a Spark ML model with Azure ML Python SDK from within Azure Databricks. For details on SDK concepts, please refer to [Private preview notebooks](https://github.com/Azure/ViennaDocs/tree/master/PrivatePreview/notebooks)

(Recommended) [Azure Databricks AML SDK notebooks](Databricks_AMLSDK_github.dbc) A single DBC package to import all notebooks in your Databricks workspace.

01. [Installation and Configuration](01.Installation_and_Configuration.ipynb): Install the Azure ML Python SDK and Initialize an Azure ML Workspace and save the Workspace configuration file.
02. [Ingest data](02.Ingest_data.ipynb): Download the Adult Census Income dataset and split it into train and test sets.
03. [Build model](03a.Build_model.ipynb): Train a binary classification model in Azure Databricks with a Spark ML Pipeline.
04. [Build model with Run History](03b.Build_model_runHistory.ipynb): Train model and also capture run history (tracking) with Azure ML Python SDK.
05. [Deploy to ACI](04.Deploy_to_ACI.ipynb): Deploy model to Azure Container Instance (ACI) with Azure ML Python SDK.
06. [Deploy to AKS](04.Deploy_to_AKS_existingImage.ipynb): Deploy model to Azure Kubernetis Service (AKS) with Azure ML Python SDK from an existing Image with model, conda and score file.

Copyright (c) Microsoft Corporation. All rights reserved. 
All notebooks in this folder are licensed under the MIT License. 
