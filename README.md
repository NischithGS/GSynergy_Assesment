Azure ETL Pipeline
-------------------
Overview
----------
This project aims to demonstrate the process of extracting, transforming, and loading (ETL) raw data from Azure Blob storage into an Azure SQL database for analysis purposes. The ETL process involves using Azure Databricks for data transformation and staging, Azure Data Factory (ADF) for orchestrating data movement, and Delta Lake for storing staged data for analytical purposes.

Process Overview
-----------------
1.Data Extraction: Raw data is sourced from Azure Blob storage. The data consists of 8 dimensions and 2 fact content files in various formats.

2.Transformation with Databricks: The raw data is ingested into Databricks notebooks for transformation. Various transformations are applied to prepare the data for analysis.

3.Staging Layer in Azure Blob: Transformed data is loaded into Azure Blob storage, serving as the staging layer for further processing.

4.Data Movement with Azure Data Factory (ADF): ADF pipelines are utilized to orchestrate data movement from the staging layer in Azure Blob storage to an Azure SQL database for analysis. This involves using activities such as GetMetadata and ForEach to efficiently load all data at once.

5.Pipeline Creation: Pipelines are created within ADF to automate the entire ETL process, ensuring seamless and efficient data movement.

6.Data Storage for Analytics: Staged data is stored in Delta Lake within Databricks. Delta Lake provides reliability, performance, and concurrency for analytics workloads.

Project Structure
------------------
src/: Contains source code for data transformation and processing in Databricks notebooks.

adf/: Includes Azure Data Factory pipeline definitions for orchestrating data movement.

sql/: Contains SQL scripts for creating tables and other database objects in Azure SQL database.

docs/: Documentation files, including this README.

Usage
------
Set up the required Azure services (Azure Blob storage, Azure SQL database, Azure Databricks, Azure Data Factory).

Configure credentials and connection strings in relevant scripts and configurations.

Execute the provided scripts and pipelines to perform the ETL process.

Analyze the data in the Azure SQL database and Delta Lake for insights and decision-making.

Dependencies
----------------
Azure Blob storage

Azure SQL database

Azure Databricks

Azure Data Factory

Prefixes of Files:
-------------------

Dim --> Code for Transforming Dimension Data

Fact --> Code for Transforming Fact Data

Delta_Lake --> Code for Pulling data into Deltalake from Staging Layer

ProjectDoc --> Brief Documentation of the ETL Pipeline

ERD_DOCUMENT --> Details of Entity Relationship Diagram of the Project

