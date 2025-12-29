# End-to-End Batch ETL Pipeline using Apache Airflow

This project demonstrates a realistic batch ETL workflow orchestrated using Apache Airflow,
designed to generate analytics-ready datasets for downstream analysis and BI reporting.

---

## Business Context

The objective of this pipeline is to process raw transactional and customer data into
clean, structured tables that can be directly consumed by analytics and dashboarding tools.

---

## Architecture Overview

Raw CSV Files  
→ Apache Airflow (Batch ETL)  
→ Analytics-Ready Tables  
→ Downstream Analysis / BI (Kaggle, Power BI, Looker, etc.)

---

## Data Sources

- `orders.csv`: Transaction-level order data
- `customers.csv`: Customer master data

---

## ETL Pipeline Design

### Extract
- Reads raw CSV files from local storage
- Performs basic schema validation
- Stores extracted snapshots for traceability

### Transform
- Deduplicates records
- Handles missing values
- Standardizes date formats
- Joins transactional and customer data
- Produces fact and dimension tables

### Load
- Writes analytics-ready datasets:
  - `fact_orders.csv`
  - `dim_customers.csv`
- Generates ETL run metadata for data quality checks

---

## Output Tables

| Table Name | Description |
|-----------|------------|
| fact_orders | Transaction-level fact table with customer attributes |
| dim_customers | Customer dimension table |
| etl_run_metadata | ETL run summary and data quality metrics |

---

## Airflow DAG

- DAG Name: `batch_etl_pipeline`
- Schedule: Daily
- Execution Type: Batch
- Catchup: Disabled

---

## Reproducibility Notes

- The pipeline is designed to run locally using Apache Airflow.
- Output datasets are versioned by ETL run and can be uploaded to Kaggle or connected to BI tools.
- This repository focuses on ETL orchestration; downstream analysis is handled separately.

---

## Tools Used

- Apache Airflow
- Python
- Pandas

---

## Author Notes

This project is intended to showcase practical ETL orchestration and analytics pipeline design,
rather than production-scale infrastructure.
