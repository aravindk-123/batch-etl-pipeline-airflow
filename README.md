# Batch ETL Pipeline using Apache Airflow

This repository showcases the design of a batch ETL pipeline orchestrated using
Apache Airflow to transform raw data into analytics-ready datasets.

> Note: This project focuses on ETL pipeline design and orchestration.
> The code is provided for reference and will be expanded further.

---

## Project Overview

The goal of this project is to demonstrate:
- Batch ETL orchestration using Apache Airflow
- Clear separation of Extract, Transform, and Load stages
- Generation of analytics-ready outputs for downstream analysis

---

## Architecture

Raw Data (CSV)  
→ Apache Airflow (ETL Orchestration)  
→ Clean Analytics Tables  
→ Downstream Analytics / BI

---

## Planned ETL Workflow

### Extract
- Read raw transactional and master data
- Perform basic schema checks

### Transform
- Deduplicate records
- Handle missing values
- Standardize date and numeric fields
- Create fact and dimension tables

### Load
- Store processed datasets
- Generate ETL metadata for data quality checks

---

## Technologies Used

- Apache Airflow
- Python
- Pandas
