
📂 Project Structure


covid-data-pipeline/

├── ingestion/

    ├── blob_to_adls_pipeline.json

    ├── http_to_adls_pipeline.json

    ├── parameterized_http_ingestion/

├── transformations/

    ├── cases_deaths_dataflow.json

    ├── hospital_admissions_dataflow.json

    ├── testing_dataflow.json

├── load/

    ├──  adls_to_azure_sql_pipeline.json



✅ Assignments & Implementation

Assignment 1: Ingest Data from Azure Blob to ADLS Gen2
Copy activity with validations and file deletion post-copy

Triggered by event-based execution

🔗 Copy Activity
🔗 Validation Activity

![image](https://github.com/user-attachments/assets/55e07353-a721-4260-ab59-6f1520d6c3f3)

Validation Activity

![image](https://github.com/user-attachments/assets/54bef68f-d294-475d-8035-e6f822ae4225)

Get Metadata Activity

![image](https://github.com/user-attachments/assets/8376f409-a3ae-44c0-9f4d-0ebd308032de)

Output:

![image](https://github.com/user-attachments/assets/54942eb1-81aa-46f8-ac1b-a2971d8e5bf8)

For Each Activity :

@activity('Get Metadata').output.childItems

![image](https://github.com/user-attachments/assets/ed150a0d-0e0f-494b-90ba-1b0c671cb39d)

![image](https://github.com/user-attachments/assets/fd0053c7-1851-43c1-b0ea-6a6157f52402)

copy activity:

Source:

![image](https://github.com/user-attachments/assets/3da9bd4f-d6e2-40ec-83be-3dc04272d14b)

Sink :

![image](https://github.com/user-attachments/assets/66a3491f-0fc6-41b5-96fa-9e80b96b6bbf)

Delete Activity :

![image](https://github.com/user-attachments/assets/f201ea1f-3ca7-4a5e-9565-41ef2ee8ffb1)

after delete activity in blob 

![image](https://github.com/user-attachments/assets/7652ec69-4414-4682-8aac-7f8d001d8dc2)


Assignment 2: Ingest Data from HTTP to ADLS Gen2
Direct copy from GitHub via HTTP

CSV: cases_deaths.csv

🔗 HTTP Linked Service

Assignment 3: Parameterized HTTP Ingestion Pipeline
Uses parameters & variables to copy multiple files:

cases_deaths.csv

hospital_admissions.csv

testing.csv

Metadata-driven using a JSON config

Executes via Lookup and ForEach activities

🔗 Lookup Activity
🔗 ForEach Activity

Assignment 4: Transform cases_deaths.csv Using Data Flows
Extract 2-digit country code

Derive cases_count, deaths_count

Rename, drop and select columns

🔗 Data Flow Overview

Assignment 5: Transform hospital_admissions.csv Using Data Flows
Split daily/weekly data

Join with country and date dimensions

Apply pivot, aggregate, conditional split, and join

Final output: weekly and daily datasets

🔗 Aggregate Transformation
🔗 Conditional Split

Assignment 6: Transform testing.csv
Add 2- and 3-digit country codes

Add week start/end date via date dimension

🔗 Join Transformation

Assignment 7: Load Transformed Data to Azure SQL
Use Copy Activity from ADLS Gen2 to Azure SQL Database

Prepare tables for Power BI reporting

🔗 Copy to Azure SQL

