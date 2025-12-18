# Azure-Data-Engineering-Pipeline-with-Medallion-Architecture
This repository presents an end to end Azure Data Engineering pipeline implemented using the Medallion Architecture. The project demonstrates secure ingestion of on premises data into Azure, scalable cloud based transformations, structured storage across multiple layers, and business intelligence visualization using Power BI. 

## Architecture Overview

<img width="2000" height="899" alt="image" src="https://github.com/user-attachments/assets/24550d9d-ca1e-4d4c-8142-cf5fc8a2f7b9" />

The pipeline is designed using the following Azure services:
* Azure Data Factory for orchestration and ingestion
* Azure Data Lake Gen2 for cloud storage
* Azure Databricks for data transformation and validation
* Azure Key Vault for secure secret management
* Power BI for business intelligence and visualization

## Medallion Architecture Design

## Bronze Layer
* Stores raw ingested data in its original format
* Acts as the system of record
* Enables reprocessing and auditing

## Silver Layer
* Contains cleaned and validated data
* Handles schema validation and null value processing
* Supports metadata driven incremental ingestion

## Gold Layer
* Stores curated and business ready datasets
* Optimized for analytical queries
* Consumed directly by Power BI dashboards

## Execution Steps

1. Deploy Azure resources
2. Configure Self Hosted Integration Runtime for Data Ingestion
3. Create and publish Azure Data Factory pipelines
4. Mount storage containers in Databricks
5. Run transformation and validation jobs
6. Visualize curated data using Power BI
