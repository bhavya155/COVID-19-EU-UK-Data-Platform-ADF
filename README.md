📊 Project Title: COVID-19 Data Platform using Azure Data Factory

  [ detailed_overview ](https://github.com/bhavya155/COVID-19-EU-UK-Data-Platform-ADF/blob/2e81f82f6ab58bd970c0bbd6a791a34118c09623/pipeline/Detailed%20Overview.md)
   
🛠 Tools & Technologies
Azure Data Factory | Azure Data Lake Gen2 | Azure Blob Storage | Power BI | Azure SQL Database | GitHub | ADF Data Flows

📄 Project Description
Designed and implemented an end-to-end data pipeline to track COVID-19 trends across EU countries and the UK. The data was sourced from public repositories (ECDC and Eurostat), transformed using Azure Data Factory Data Flows, and loaded into Azure SQL Database to enable Power BI-based reporting and analytics.

🔍 Detailed Workflow
Data Ingestion: Retrieved daily and weekly COVID-19 datasets (cases, deaths, hospitalizations, tests, and population data) from Azure Blob and HTTP endpoints using parameterized ADF pipelines.

Validation: Performed metadata validation and file integrity checks using ADF control flow activities (Validation, Get Metadata, If Condition).

Data Transformation: Applied transformations such as pivoting, filtering, joining with dimension tables (country, date), renaming columns, and splitting data based on frequency (daily/weekly) using ADF Data Flows.

Automation: Used Lookup and ForEach activities with a JSON-driven metadata file to automate ingestion and transformation for multiple datasets.

Date Enrichment: Incorporated a Date Dimension table to calculate and attach week start/end dates for weekly datasets.

Data Loading: Loaded processed data into Azure SQL Database for reporting purposes.
