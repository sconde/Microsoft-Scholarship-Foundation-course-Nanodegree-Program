Cloud Services for Machine Learning
===================================

A typical cloud service for machine learning provides support for managing the core assets involved in machine learning projects. For your reference, you can see a table summarizing these main **assets** below. We'll explore all of these components in more detail as we go through the course.

| Feature            | Description                                                                                   |
| ---                | ---                                                                                           |
| Datasets           | Define, version, and monitor datasets used in machine learning runs.                          |
| Experiments / Runs | Organize machine learning workloads and keep track of each task executed through the service. |
| Pipelines          | Structured flows of tasks to model complex machine learning flows.                            |
| Models             | Model registry with support for versioning and deployment to production.                      |
| Endpoints          | Expose real-time endpoints for scoring as well as pipelines for advanced automation.          |


Machine learning cloud services also need to provide support for **managing** the resources required for running machine learning tasks:

| Feature      | Description                                                                                                     |
| ---          | ---                                                                                                             |
| Compute      | Manage compute resources used by machine learning tasks.                                                        |
| Environments | Templates for standardized environments used to create compute resources.                                       |
| Datastores   | Data sources connected to the service environment (e.g. blob stores, file shares, Data Lake stores, databases). |


A Brief Intro to Azure Machine Learning
---------------------------------------

Below are some of the features of Azure Machine Learning that we just discussed. We'll get some hands-on experience using these features during the labs found throughout this course. For now, our goal is just to take a brief tour of the main features.

Following are some of the features in **Azure ML workspace**, a centralized place to work with all the artifacts you create:

| Feature      | Description                                                                                                                                            |
| ---          | ---                                                                                                                                                    |
| Automated ML | Automate intensive tasks that rapidly iterate over many combinations of algorithms, hyperparameters to find the best model based on the chosen metric. |
| Designer     | A drag-and-drop tool that lets you create ML models without a single line of code.                                                                     |
| Datasets     | A place you can create datasets.                                                                                                                       |
| Experiments  | A place that helps you organize your runs.                                                                                                             |
| Models       | A place to save all the models created in Azure ML or trained outside of Azure ML.                                                                     |
| Endpoints    | A place stores real-time endpoints for scoring and pipeline endpoints for advanced automation.                                                         |
| Compute      | A designated compute resource where you run the training script or host the service deployment.                                                        |
| Datastores   | An attached storage account in which you can store datasets.                                                                                           |


### Quiz Question

Below are some of the features we just went over. Can you match each one with its description?


The designer: 
A drag-and-drop tool that lets you create machine learning models without writing any code.

The Azure ML workspace: 
A centralized place to work with all the artifacts you create.

Computer target: 
A designated resource/environment where you run your training script or host your service deployment.

Data store: 
Attached storage account in which you can keep data for your machine learning workspace.

