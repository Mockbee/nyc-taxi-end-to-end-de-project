# **Green Taxi Trip Data Engineering Project**

In this project, we designed and implemented a modern data pipeline using **Azure Data Factory**, **Databricks**, **Azure Data Lake**, and **Power BI**, structured around the Medallion Architecture.

---

### **Project Architecture**
![Architecture Diagram](https://github.com/Mockbee/nyc-taxi-end-to-end-de-project/blob/main/Screenshot%202024-12-22%20174534.png)

---

### **About Dataset/API Used**
This project integrates data from two diverse sources:  
1. **CSV files** containing Green Taxi trip data.  
   - The dataset can be accessed [here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).  
2. **A public API** providing additional datasets, such as trip_type and trip_zone.  

These datasets were processed to build a scalable pipeline for insights and analytics.

---

### **Services and Tools Used**

1. **Azure Data Lake:**  
   - Centralized repository for storing raw, processed, and enriched data.  
   - Ensures scalability and efficient storage using service principals for role-based access control.

2. **Databricks:**  
   - Cloud-based platform for big data processing and machine learning.  
   - Used for PySpark-based data transformations and creating Delta tables.

3. **Azure Data Factory (ADF):**  
   - Orchestrated data pipelines with activities like Copy, ForEach, and conditional logic (If-Else).  
   - Implemented dynamic pipelines using parameters for diverse dataset processing.

4. **Delta Lake:**  
   - Enables advanced features like versioning, transaction logs, and time travel for querying historical data states.

5. **Power BI:**  
   - Connected to Databricks for creating dynamic dashboards and visualizations from enriched data in the Gold Layer.

---

### **Project Execution Flow**

1. **Bronze Layer (Raw Data Ingestion):**  
   - Data from the CSV files and API was ingested into Azure Data Lake.  
   - Stored in **CSV** and **Parquet** formats for initial processing.

2. **Silver Layer (Data Transformation):**  
   - Raw data was cleaned and transformed into a structured, queryable format.  
   - Stored in **Parquet format** for optimized performance.

3. **Gold Layer (Data Enrichment):**  
   - Enriched data was stored in **Delta format**, leveraging its advanced capabilities for analytics.  
   - Features like tombstoning, transaction logs, and versioning were utilized.

4. **Data Orchestration Using ADF:**  
   - Pipelines orchestrated the entire data ingestion process with activities like `Copy` and `GetMetadata`.  
   - Dynamic pipelines allowed processing of multiple datasets efficiently.

5. **Data Processing with Databricks:**  
   - Connected Databricks to Azure Data Lake using service principal authentication.  
   - PySpark scripts applied complex transformations and loaded data into Delta tables.

6. **Data Visualization with Power BI:**  
   - Imported Gold Layer data into Power BI to create actionable dashboards and visualizations.

---

### **Key Features**
- **Scalable Architecture:** Leveraged Medallion Architecture for effective data organization.  
- **Dynamic Pipelines:** Enabled flexible data ingestion and transformation using Azure Data Factory.  
- **Optimized Storage Formats:** Used CSV, Parquet, and Delta formats to balance storage and performance.  
- **Delta Lake Features:** Advanced analytics capabilities like time travel and transaction management.

---

This project highlights the application of modern data engineering practices to extract, transform, and analyze data efficiently, turning raw datasets into actionable insights.
