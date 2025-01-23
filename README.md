# End-to-End Data Engineering: Tokyo Olympics Project🏅

📖 Overview
This project is an end-to-end data engineering solution to analyze the Tokyo Olympics 2021 data, sourced from Kaggle. The project leverages modern cloud tools for data storage, ingestion, processing, warehousing, and visualization. The final output is an interactive dashboard in Power BI, offering insights into the performance of the 2021 Tokyo Olympics.

🚀 Features
- Data Ingestion: Seamless data pipeline using Azure Data Factory.
- Data Processing: Scalable transformations with Azure Databricks.
- Data Warehousing: Efficient storage and querying using Azure Synapse Analytics.
- Visualization: Insightful and interactive dashboard with Power BI.

📁 Dataset
Dataset Name: 2021 Olympics in Tokyo
Source: Kaggle


🛠️ Tools & Technologies Used
- Azure Data Factory: For data ingestion pipelines.
- Azure Data Lake Storage Gen2: To store raw and processed data.
- Azure Databricks: For data transformation and ETL.
- Azure Keyvault: For storing credentials and important information
- Azure Synapse Analytics: For creating a lake database and data warehousing.
- Power BI: For data visualization.


📊 Project Architecture & Pipeline
![Architecture of the data pipeline](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/pipeline.gif) 
Below is the high-level architecture of the project:
1. Data Ingestion:
   - Used Azure Data Factory to fetch data from a GitHub repository and load it into Azure Data Lake Storage Gen2.
2. Data Processing:
  - Processed the raw data in Azure Databricks, performed transformations, and stored the processed data back into the data lake.
3. Data Warehousing:
  - Created a Lake Database in Azure Synapse Analytics for structured querying.
4. Visualization:
  - Connected Power BI to Synapse Analytics to build interactive visuals and dashboards.
