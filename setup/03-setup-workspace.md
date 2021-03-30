# Setup the Lab 03 AI-in-a-Day workspace

## Task 1 - Create a Machine Learning Workspace

## Task 2 - Create an Azure Databricks Workspace

- **Name**: `ai-adb-ws`
- **Pricing Tier**: `Premium (+ Role-based access controls)`

## Task 3 - Create ADB Cluster

- **Name**: `ai-adb-lab`

- **Databricks Runtime Version**: `7.3 LTS ML (includes Apache Spark 3.0.1, Scala 2.12)`

- **Enable autoscaling**: `Unchecked`

- **Worker Type**: `Standard_DS4_v2`

- **Workers**: `1`

- **Advanced Options/Spark/Environment Variables**
    - PYSPARK_PYTHON=/databricks/python3/bin/python3
    - AML_SUB_ID=xxx-xxx-xxx
    - AML_RG=xxx-xxx-xxx
    - AML_WS=xxx-xxx-xxx

>> Important please provide the `subscription_id`, `resource_group`, and `workspace_name` for the Azure Machine Learning workspace created in Step #1.

![Create ADB Cluster](media/adb-cluster-1.png)

## Task 4 - Install Libraries on the ADB cluster

**Install Library/PyPI**
- langdetect==1.0.8
- seaborn==0.11.1
- nltk==3.5
- fairlearn==0.4.6
- shap==0.37.0
- joblib==1.0.0
- azureml-sdk[databricks]
- azureml-contrib-fairness
- textblob==0.15.3

![Install Libraries on the ADB cluster](media/adb-cluster-2.png)

## Task 5 - Upload the Databricks notebook archive

Upload the notebooks archive (`AI-Lab3.dbc`) from the following location to the user's folder in Azure Databricks workspace:

[AI-Lab3.dbc](https://github.com/solliancenet/ai-in-a-day/blob/main/03-ml-in-databricks/notebooks/AI-Lab3.dbc?raw=true)

## Task 6 - Copy lab data files to storage account

**Source location**
- Subscription: **Synapse Analytics Demos and Labs**
- Resource group: **Synapse-Analytics-Data**
- Storage account: **solliancepublicdata**
- Container: **ai-in-a-day**
- Folder: **Shared**

**Destination location**
- Storage account: **aiinadaystorageXXXXXX**
- Container: **lab-03**
- Folder: **Shared**

All the files in the destination folder need **public read access**.
