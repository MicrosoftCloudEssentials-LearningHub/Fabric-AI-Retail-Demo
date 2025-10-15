# Demo: Retail Intelligence with Fabric - Overview

> Exploring Microsoft Fabric’s capabilities and AI readiness.


Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-10-09

------------------------------------------

> [!TIP]
> Click to read more about [Fabric Roadmap](https://roadmap.fabric.microsoft.com/?product=administration%2Cgovernanceandsecurity)

> [!IMPORTANT]
> For more detailed and official training, please visit the [Microsoft official training site](https://learn.microsoft.com/en-us/training/)

<details>
<summary><b>List of references</b> (Click to expand)</summary>
  
- [Microsoft Fabric decision guide: copy activity, Copy job, dataflow, Eventstream, or Spark](https://learn.microsoft.com/en-us/fabric/fundamentals/decision-guide-pipeline-dataflow-spark)
- [Microsoft Fabric decision guide: Choose a data integration strategy](https://learn.microsoft.com/en-us/fabric/data-factory/decision-guide-data-integration?toc=%2Ffabric%2Ffundamentals%2Ftoc.json&bc=%2Ffabric%2Ffundamentals%2Fbreadcrumb%2Ftoc.json)

    <img width="1115" height="725" alt="image" src="https://github.com/user-attachments/assets/ef1db682-1673-421e-a9cf-370894ce7be3" />

- [Microsoft Fabric decision guide: Choose a data movement strategy](https://learn.microsoft.com/en-us/fabric/data-factory/decision-guide-data-movement?toc=%2Ffabric%2Ffundamentals%2Ftoc.json&bc=%2Ffabric%2Ffundamentals%2Fbreadcrumb%2Ftoc.json)

    <img width="1532" height="842" alt="image" src="https://github.com/user-attachments/assets/7f95b1c9-9eb9-4b66-89a7-13c3fa046269" />

- [Microsoft Fabric decision guide: choose a data store](https://learn.microsoft.com/en-us/fabric/fundamentals/decision-guide-data-store
)

    <img width="523" height="465" alt="image" src="https://github.com/user-attachments/assets/ca15f8b9-6c96-4bc5-9d27-66f65afe31e2" />

- [Microsoft Fabric decision guide: Choose between Warehouse and Lakehouse](https://learn.microsoft.com/en-us/fabric/fundamentals/decision-guide-lakehouse-warehouse)

    <img width="1610" height="483" alt="image" src="https://github.com/user-attachments/assets/5aa282f3-4202-4195-8376-2c071c88d90d" />

- [Zava DIY Dataset Plus MCP](https://github.com/microsoft/ai-tour-26-zava-diy-dataset-plus-mcp/tree/main) - github repo

</details>

<details>
<summary><b>Table of Content </b> (Click to expand)</summary>
  
- [How to setup](#how-to-setup)
- [Prerequisites](#prerequisites)
- [Where to start?](#where-to-start)
- [Content](#content)

</details>

> Before Fabric

<p float="left">
  <img src="https://github.com/brown9804/MSCloudEssentials_LPath/assets/24630902/c47ad7c0-375e-4257-b56e-7b3b89619e2f" width="450" height="200" />
  <img src="https://github.com/user-attachments/assets/1cbb0198-774c-498d-ab60-2f4c8e2a4218" width="350" height="190" />
</p>

> E.g of a solution prior Microsoft Fabric:

<div align="left">
  <img src="https://github.com/user-attachments/assets/af2aa6cb-0349-481b-abe4-d8c470551899" 
       alt="Centered Image" 
       style="width: 70%; border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>

> Now from one place:

<div align="left">
  <img src="https://github.com/user-attachments/assets/aaf00cd7-531a-4dc8-bf2f-c7606c607b87" 
       alt="Centered Image" 
       style="width: 70%; border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>

<div align="left">
  <img src="https://github.com/user-attachments/assets/8fdb3198-8fda-4dd0-869e-b0dccb268a30" 
       alt="Centered Image" 
       style="width: 70%; border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>

From [Microsoft Documentation](https://learn.microsoft.com/pt-br/fabric/fundamentals/microsoft-fabric-overview)

<details>
<summary><b>Workloads overview</b> (Click to expand)</summary>
  
| Component                | Purpose                                      | Key Features                                                                 | Why Fabric vs. Each Resource Individually                                  |
|--------------------------|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| **Data Factory**         | Cloud-based data integration service         | Orchestrates and automates data movement and transformation. Supports ETL processes. | **Enhanced Integration**: Fabric integrates Data Factory with other components, reducing data silos and improving workflow efficiency. |
| **Synapse Data Engineering** | Big data processing                        | Utilizes Apache Spark for large-scale data preparation and transformation. Integrates with various data sources. | **Unified Platform**: Fabric provides a cohesive environment where data engineering seamlessly connects with analytics and other services, streamlining data processing and reducing complexity. |
| **Synapse Data Warehouse** | Scalable analytics service                  | Combines big data and data warehousing. Provides high-performance SQL-based analytics. | **Comprehensive Insights**: Fabric's integration allows for unified analytics, offering a holistic view of data across different services, enhancing decision-making and operational efficiency. |
| **Synapse Real-Time Analytics** | Real-time data analytics                | Processes streaming data for immediate insights. Supports real-time dashboards and alerts. | **Seamless Data Flow**: Fabric ensures continuous data flow and real-time analytics integration, enhancing responsiveness and enabling proactive decision-making. |
| **Power BI**             | Business analytics tool                      | Interactive visualizations, self-service BI capabilities. Allows users to create reports and dashboards easily. | **Enhanced Connectivity**: Fabric enhances Power BI's capabilities by providing better data connectivity and integration with other components, leading to richer insights and more comprehensive reporting. |
| **Data Activator**       | Trigger actions based on data conditions     | Automates responses to specific data events. Enhances data-driven decision-making. | **Integrated Automation**: Fabric leverages comprehensive data insights for more effective automation and action-triggering, improving operational efficiency and responsiveness. |
| **Synapse Data Science** | Machine learning and data science            | Tools for building, training, and deploying ML models. Integrates with the Synapse ecosystem for scalable data science workflows. | **Unified Workflows**: Fabric integrates data science workflows with other Synapse services, enhancing collaboration, scalability, and the ability to derive actionable insights from data. |

</details>


## How to setup

> Overall, you can set up your infrastructure using either of the following approaches:

1. [Infrastructure via Azure Portal](./AzurePortal/) (`Click Ops`): This approach involves creating the infrastructure and performing `all necessary steps through the Azure Portal` and its resources interface. 
2. [Infrastructure via Terraform](./Terraform/) (`IaC`, like Bicep or ARM Templates): This approach focuses on `setting up the required infrastructure via Terraform`. It allows for source control of not only the solution code, connections, and setups `but also the infrastructure itself`.

<div align="center">
  <img src="https://github.com/user-attachments/assets/16640052-7f57-443a-9efd-30855de5e231" alt="Centered Image" style="border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>

## Prerequisites

- An `Azure subscription is required`. All other resources, including instructions for creating a Resource Group, are provided in this workshop.
- `Contributor role assigned or any custom role that allows`: access to manage all resources, and the ability to deploy resources within subscription.
- If you choose to use the Terraform approach, please ensure that:
    -  [Terraform is installed on your local machine](https://developer.hashicorp.com/terraform/tutorials/azure-get-started/install-cli#install-terraform).
    -  [Install the Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) to work with both Terraform and Azure commands.


## Where to start? 

This is an introductory workshop on Microsoft Fabric. Please follow as described below.

- If you're choosing the [Infrastructure via Azure Portal](./AzurePortal/):
    1. Go through [each section](#content) `from the start`.
- If you're choosing the [Infrastructure via Terraform](./Terraform/) approach:
    1. Please follow the [Terraform guide](./Terraform/README.md) to deploy the necessary Azure resources for the workshop.
    2. Then, follow each [each section](#content) but `skip the creation of each resource`.
       
## Content 

- [Medallion Architecture](./AzurePortal/1_MedallionArch/): Explore the structured approach to data management.

    <div align="center">
      <img src="https://github.com/user-attachments/assets/2c5141ea-4f3a-4054-b8bd-313efde24ff0" alt="Centered Image" style="border: 2px solid #4CAF50; border-radius: 2px; padding: 2px; width: 900px; height: auto;"/>
    </div>

- [AI + LLMs](./AzurePortal/2_AI_LLMs/): Discover how artificial intelligence and large language models integrate with Fabric.
  - Example of [how to integrate Azure OpenAI with Fabric](https://github.com/MicrosoftCloudEssentials-LearningHub/Fabric-AI-Retail-Demo/tree/main/AzurePortal/2_AI_LLMs#configure-azure-openai-service): Call a deployed model and request information.
  - [Basic Usage of LangChain Transformer](https://github.com/MicrosoftCloudEssentials-LearningHub/Fabric-AI-Retail-Demo/tree/main/AzurePortal/2_AI_LLMs#basic-usage-of-langchain-transformer): Create a prompt template, set up an LLMChain, and configure the transformer to execute the processing chain.
  - Example of [Using LangChain for Large Scale Literature Review](https://github.com/MicrosoftCloudEssentials-LearningHub/Fabric-AI-Retail-Demo/tree/main/AzurePortal/2_AI_LLMs#using-langchain-for-large-scale-literature-review): This example is around extracting content from PDFs linked in arXiv papers and generating prompts for extracting specific information.
  - [Machine Learning Integration with Microsoft Fabric](https://github.com/MicrosoftCloudEssentials-LearningHub/Fabric-AI-Retail-Demo/tree/main/AzurePortal/2_AI_LLMs#machine-learning-integration-with-microsoft-fabric): Shows how to train and register machine learning models using Microsoft Fabric's native integration with the MLflow framework. This includes logging trained models, hyperparameters, and evaluation metrics. It also shows how to compare and filter machine learning models using MLflow, with an example using RandomForestRegressor.

- [Data Agent](./AzurePortal/3_DataAgent.md): Get insights on using AI skills within the platform.

    <img width="1141" height="669" alt="image" src="https://github.com/user-attachments/assets/7c9cac60-8048-4a02-bc5a-c81ba5c041e1" />

- `DevOps`: Learn about continuous integration and continuous deployment, including [deployment pipelines](./AzurePortal/4_DevOps/0_deployment-pipelines/) and [GitHub integration](./AzurePortal/4_DevOps/1_github-integration.md).

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-1418-limegreen" alt="Total views">
  <p>Refresh Date: 2025-10-09</p>
</div>
<!-- END BADGE -->
