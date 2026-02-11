# End-to-End Databricks Data Engineering Project

## Overview
This project demonstrates an end-to-end data engineering pipeline built using Databricks and PySpark.
The objective is to process data from multiple child companies, handle schema inconsistencies, and
create a unified Gold layer dataset suitable for analytics.

## Business Scenario
The project simulates a parent company receiving data from multiple child companies where data
structures are inconsistent and not analytics-ready. The pipeline standardizes and combines this
data into a single, reliable dataset.

## Architecture
- Data Source: AWS S3
- Processing Engine: Databricks (PySpark)
- Storage Layers: Bronze, Silver, Gold
- Data Format: Delta Lake

## Data Processing Flow
1. **Bronze Layer**
   - Ingests raw data from AWS S3.
   - Stores data in its original format with minimal transformation.

2. **Silver Layer**
   - Cleans and standardizes data from different child companies.
   - Processes dimension data by resolving schema mismatches and data quality issues.

3. **Gold Layer**
   - Combines cleaned dimension and fact data.
   - Creates analytics-ready tables for reporting and downstream use.

## Fact Data Processing
- Supports both historical data loads and incremental data processing.
- Ensures fact tables remain accurate and up to date.

## Orchestration
- Pipeline execution is orchestrated to ensure Bronze → Silver → Gold processing order.
- Designed for reliable and repeatable data processing workflows.

## Tech Stack
- Databricks
- PySpark
- AWS S3
- Delta Lake

## How to Use
1. Upload source data to AWS S3.
2. Configure S3 access in Databricks.
3. Execute notebooks/scripts in the following order:
   - Bronze ingestion
   - Silver transformations
   - Gold aggregation

## Notes
- Sample data is not included to keep the repository lightweight.
- The project focuses on data processing logic and architecture.

