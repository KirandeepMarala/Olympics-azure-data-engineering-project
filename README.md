# End-to-End Data Engineering: Tokyo Olympics Project🏅

## 📖 Overview
This project is an **end-to-end data engineering solution** to analyze the Tokyo Olympics 2021 data, sourced from Kaggle. The project leverages modern cloud tools for data storage, ingestion, processing, warehousing, and visualization. The final output is an interactive dashboard in **Power BI**, offering insights into the performance of the 2021 Tokyo Olympics.

---

## 📁 Dataset
- **Dataset Name**: 2021 Olympics in Tokyo  
- **Source**: [Kaggle](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo)

---

## 🛠️ Tools & Technologies Used
- **Azure Data Factory**: For data ingestion pipelines.
- **Azure Data Lake Storage Gen2**: To store raw and processed data.
- **Azure Databricks**: For data transformation and ETL.
- **Azure Key Vault**: For securely storing credentials and sensitive information.
- **Azure Synapse Analytics**: For creating a lake database and data warehousing.
- **Power BI**: For data visualization.

---

## 📊 Project Architecture & Pipeline
![Architecture of the data pipeline](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/pipeline.gif) 

Below is the high-level architecture of the project:

1. **Data Ingestion**:
   - Used **Azure Data Factory** to fetch data from a GitHub repository and load it into **Azure Data Lake Storage Gen2**.
2. **Data Processing**:
   - Processed the raw data in **Azure Databricks**, performed transformations, and stored the processed data back into the data lake.
3. **Data Warehousing**:
   - Created a **Lake Database** in **Azure Synapse Analytics** for structured querying.
4. **Visualization**:
   - Connected **Power BI** to Synapse Analytics to build interactive visuals and dashboards.

---


## ⚙️ Step-by-Step Implementation

### 1. Data Ingestion with Azure Data Factory
![datafactory pipeline](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/datafactory_pipeline.png) 
- Created a **data pipeline** to ingest data from a public GitHub repository.  
- Used a **parameterized approach**, with lookups and **For Each** activity to copy multiple files.  
- Stored the raw data in **Azure Data Lake Storage Gen2**.



### 2. Data Processing with Azure Databricks
- Mounted the ADLS storage to Databricks using **dbutils** and created a **secret scope** for secure access.  
- Used **PySpark** in Databricks to clean and transform the raw data.  
- Below transformations were performed:
  - Changed column names to appropriate names.
  - Replaced null values with appropriate defaults.
  - Checked and removed duplicate rows.
  - Changed data types for consistency.
  - Added a new column: **country codes**.
- Processed data was written back to **Azure Data Lake Storage Gen2** in a structured **Parquet** format.  
- **Screenshot**:  
  *(Add your screenshot here)*  

### 3. Data Warehousing with Azure Synapse Analytics
- Created a **Lake Database** in **Azure Synapse Analytics** to query transformed data.  
- Used **SQL Serverless Pool** for data analysis.  
- **Screenshot**:  
  *(Add your screenshot here)*  

### 4. Data Visualization with Power BI
- Connected **Power BI** to Synapse Analytics to build interactive dashboards.  
- **Key Visuals**:
  - Medal count by country.
  - Athlete performance by sport.
  - Gender-wise medal distribution.  
---

## 📊 Sample Power BI Visuals
- **Visual 1**: Medal Distribution by Country  
  *(Add your visual here)*  

- **Visual 2**: Athlete Performance by Sport  
  *(Add your visual here)*  

- **Visual 3**: Gender-wise Medal Count  
  *(Add your visual here)*  

---
