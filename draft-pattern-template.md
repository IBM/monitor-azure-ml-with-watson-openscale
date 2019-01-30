# Monitor Azure ML With AI OpenScale

# Create a Machine Learning Model with Azure and Monitor Payload Logging and Fairness using AI OpenScale

# Author

* Lukasz Cmielowski lukasz.cmielowski@pl.ibm.com
* Scott D'Angelo scott.dangelo@ibm.com

# URLs

### Github repo

* https://github.com/IBM/monitor-azure-ml-with-ai-openscale

# Summary

In this Code Pattern, we will use fictional sales data to create a logistic regression model using Azure. We will use AI OpenScale to bind the ML model deployed in the Azure cloud, create a subscription, and perform payload and feedback logging.

When the reader has completed this Code Pattern, they will understand how to:

* Prepare data, train a model, and deploy using Azure
* Score the model using sample scoring records and the scoring endpoint
* Setup AI OpenScale Data Mart
* Bind the Azure model to the AIOS Data Mart
* Add subscriptions to the Data Mart
* Enable payload logging and performance monitor for both subscribed assets
* Use Data Mart to access tables data via subscription

# Technologies

* [Analytics](https://developer.ibm.com/watson/): Analytics delivers the value of data for the enterprise.
* [Artificial Intelligence](https://medium.com/ibm-watson): Artificial intelligence can be applied to disparate solution spaces to deliver disruptive technologies
* [Data Science](https://medium.com/ibm-watson): Systems and scientific methods to analyze structured and unstructured data in order to extract knowledge and insights.

# Description

This pattern describes a method to use AI OpenScale and a Azure machine learning model .With AI OpenScale, we can monitor model quality and log payloads, regardless of where the model is hosted. In this case, we use the example of an Azure model , which demonstrates the agnostic and open nature of AI OpenScale (AIOS).

IBM AI OpenScale is an open environment which enables organizations to automate and operationalize their AI.  OpenScale provides a powerful platform for managing AI and ML models on the IBM cloud, or wherever they may be deployed, offering these benefits:

Open by design: AI OpenScale allows monitoring and management of ML and DL models built using any frameworks or IDEs and deployed on any model hosting engine.

Drive fairer outcomes: AI OpenScale detects and helps mitigate model biases to highlight fairness issues. The platform provides plain text explanation of the data ranges which have been impacted by bias in the model, and visualizations helping data scientists and business users understand the impact on business outcomes. As biases are detected, AI OpenScale automatically creates a de-biased companion model that runs beside deployed model, thereby previewing the expected fairer outcomes to users without replacing the original.

Explain transactions: AI OpenScale helps enterprises bring transparency and auditability to AI-infused applications by generating explanations for individual transactions being scored, including the attributes that were used to make the prediction and weightage of each attribute.

Automate the creation of AI: Neural Network Synthesis (NeuNetS), available in this update as a beta, synthesizes neural networks by fundamentally architecting a custom design for a given data set. In the beta, NeuNetS will support image and text classification models. NeuNetS reduces the time and lowers the skill barrier required to design and train custom neural networks, thereby putting neural networks within the reach of non-technical subject matter experts, as well as making data scientists more productive.

# Flow

![](doc/source/images/architecture.png)

1. The developer creates a Jupyter Notebook.
2. The Jupyter Notebook is connected to a PostgreSQL database, which is used to store AI OpenScale data.
3. An ML model is created using Azure ML Studio, using data from [GoSales_Tx](https://github.com/IBM/monitor-azure-ml-with-ai-openscale/data/GoSales_Tx.csv),  and then it is deployed to the cloud.
4. AI Open Scale is used by the notebook to log payload and monitor performance.

# Instructions

> Find the detailed steps for this pattern in the [readme file](https://github.com/IBM/monitor-sagemaker-ml-with-ai-openscale/blob/master/README.md). The steps will show you how to:

1. Clone the repository
2. Create a Compose for PostgreSQL DB
3. Create an AI OpenScale service
4. Run the notebooks

# Components and services

* [AI OpenScale](https://console.bluemix.net/catalog/services/ai-openscale)
* IBM PostgreSQL
* [Jupyter Notebook](https://jupyter.org/)

# Runtimes

* Python 3.5

# Related links

* [Deploy a Custom Machine Learning engine using Docker and Kubernetes, and Monitor Payload Logging and Fairness using AI OpenScale](https://developer.ibm.com/patterns/monitor-custom-machine-learning-engine-with-ai-openscale/)
* [Predict heart medicine using machine learning](https://developer.ibm.com/patterns/predict-heart-medicine-using-machine-learning/)
* [Monitor performance, fairness, and quality of a WML model with AI OpenScale APIs](https://developer.ibm.com/patterns/monitor-performance-fairness-and-quality-of-a-wml-model-with-ai-openscale-apis/)

# Announcement

The focus of this code pattern is to gain insights into a machine learning model using IBM AI OpenScale. The pattern provides examples of how to configure the OpenScale service, as well as how to utilize AI OpenScale with Azure.

IBM AI OpenScale is an open platform which enables organizations to automate and operate their AI across its full lifecycle. OpenScale provides a powerful platform for managing AI and ML models on IBM Cloud or IBM Cloud Private, or wherever they may be deployed, offering these benefits:

Open by design: AI OpenScale provides insights into the health of ML and DL models – their performance, as well as accuracy and fairness of outcomes – built using any frameworks or IDEs, and deployed on any model hosting engine.

Drive fairer outcomes: AI OpenScale detects and helps mitigate model biases to highlight possible fairness issues. The platform provides plain text explanations of the data ranges which have been impacted by bias in the model, and visualizations to help data scientists and business users understand the impact on business outcomes. As biases are detected, AI OpenScale automatically creates a de-biased companion model that runs beside deployed model, thereby previewing the expected fairer outcomes to users, without replacing the original model.

Explain transactions: AI OpenScale helps enterprises bring transparency and auditability to AI-infused applications by generating explanations for individual transactions, including the attributes that were used to make the prediction and weightage of each attribute.

Automate the creation of AI: Neural Network Synthesis (NeuNetS), available in this update as a beta, automatically synthesizes neural networks by fundamentally architecting a custom design for a given data set. In the beta, NeuNetS will support image and text classification models. NeuNetS reduces the time and lowers the skill barrier required to design and train custom neural networks, thereby putting neural networks further within the reach of non-technical subject matter experts, as well as making data scientists more productive.

Read More:

[AI OpenScale service on IBM Cloud](https://console.bluemix.net/catalog/services/ai-openscale)
[More Details on AI OpenScale Functionality](https://www.ibm.com/blogs/bluemix/2018/12/automate-and-operationalize-your-ai-with-ai-openscale/)

