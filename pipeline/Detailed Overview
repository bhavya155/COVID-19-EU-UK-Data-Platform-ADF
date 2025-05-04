
📂 Project Structure

covid-data-pipeline/
├── ingestion/
│   ├── blob_to_adls_pipeline.json
│   ├── http_to_adls_pipeline.json
│   ├── parameterized_http_ingestion/
├── transformations/
│   ├── cases_deaths_dataflow.json
│   ├── hospital_admissions_dataflow.json
│   ├── testing_dataflow.json
├── load/
    └── adls_to_azure_sql_pipeline.json


✅ Assignments & Implementation

Assignment 1: Ingest Data from Azure Blob to ADLS Gen2
Copy activity with validations and file deletion post-copy

Triggered by event-based execution

🔗 Copy Activity
🔗 Validation Activity

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

