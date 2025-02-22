# End-to-End Data Engineering: Tokyo Olympics Project🏅

## 📖 Overview
This project is an **end-to-end data engineering solution** to analyze the Tokyo Olympics 2021 data, sourced from Kaggle. The project leverages modern cloud tools for data storage, ingestion, processing, warehousing, and visualization. The final output is an interactive dashboard in **Power BI**, offering insights into the performance of the 2021 Tokyo Olympics.

---

## 📁 Dataset
- **Dataset Name**: 2021 Olympics in Tokyo  
- **Source**: [Kaggle](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo)

---

## 🛠️ Tools & Technologies Used
![All Resources](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/all_resources.png)
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
![databricks mount tables](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/azure_databricks.png) 
- Mounted the ADLS storage to Databricks using **dbutils** and created a **secret scope** for secure access.  
- Used **PySpark** in Databricks to clean and transform the raw data.  
- Below transformations were performed:
  - Changed column names to appropriate names.
  - Replaced null values with appropriate defaults.
  - Checked and removed duplicate rows.
  - Changed data types for consistency.
  - Added a new column: **country codes**.
- Processed data was written back to **Azure Data Lake Storage Gen2** in a structured **Parquet** format.  

### 3. Data Warehousing with Azure Synapse Analytics
<div align="center">
  <img src="https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/lake_database.png" alt="lake database">
</div>

- Created a **Lake Database** in **Azure Synapse Analytics** to query transformed data.  
- Used **SQL Serverless Pool** for data analysis.

### 4. Data Visualization with Power BI
![Medals Analysis](https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project/blob/main/Images/dashboard_medals_performances.png) 
- Connected **Power BI** to Synapse Analytics to build interactive dashboards.
- Live Interactive Report Link: [Click Here](https://app.powerbi.com/view?r=eyJrIjoiYjE3OTUwYTQtNWJjZi00ODM3LTk5ZTItMTk5NDFlOTFkNDhkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)
---

## 📜 How to Run This Project

1. **Clone the Repository:**
```bash
git clone https://github.com/KirandeepMarala/Olympics-azure-data-engineering-project.git
 ```
2. **Set Up Azure Resources**: Provision Azure Data Factory, Data Lake, Databricks, and Synapse Analytics.
     
3. **Configure Pipelines**: Import the Data Factory pipeline JSON and configure the GitHub data source.
     
4. **Run Databricks Notebooks**: Execute transformations and load the processed data back to ADLS.
5. **Create Lakedatabase**: Using Synapse analytics, create lake database.
6. **Connect Power BI**: Use the Power BI desktop to connect to Synapse and build visuals.
---

## 🙏 Credits & Acknowledgments

This project was guided and inspired by a tutorial from **Darshil Parmar** on his YouTube channel. His comprehensive and insightful content helped in shaping this end-to-end data engineering pipeline.  

You can watch the tutorial here: [End-to-End Azure Data Engineering Project - Darshil Parmar](https://www.youtube.com/watch?v=IaA9YNlg5hM)

A big thanks to him for creating such a detailed and helpful resource!

---

## 🎯 Conclusion
This project demonstrates a comprehensive **data engineering pipeline**, showcasing how to process, store, and visualize data in a cloud-native ecosystem. The **Power BI report** provides an intuitive way to explore and understand Tokyo Olympics 2021 data.

Feel free to reach out for any questions or suggestions! 😊

---

## 📬 Contact

- **Author**: [kirandeep Marala](#)
- **Email**: [kirandeep.marala@gmail.com](mailto:kirandeep.marala@gmail.com)
- **LinkedIn**: [My LinkedIn Profile](https://www.linkedin.com/in/kirandeepmarala/)

---
