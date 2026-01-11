# 🚀 AWS Bronze–Silver–Gold COVID Data Pipeline

An end-to-end **AWS Data Engineering pipeline** implementing the **Bronze → Silver → Gold** lakehouse architecture using **Amazon S3, AWS Glue (PySpark), Amazon Athena, and Amazon Redshift** to ingest, transform, validate, and analyze COVID-19 data at scale.

This project demonstrates **real-world, production-style data engineering best practices** including layered storage, scalable Spark ETL, data validation, and analytics-ready modeling.

---

## 📌 Project Overview

This pipeline processes raw COVID-19 data and converts it into clean, validated, and analytics-ready datasets.

### What the pipeline does:
- Ingests raw COVID data into Amazon S3 (Bronze layer)
- Cleans and standardizes data using AWS Glue PySpark jobs (Silver layer)
- Aggregates data for analytics (Gold layer)
- Validates datasets using Amazon Athena
- Runs analytical queries using Amazon Redshift

---

## 🧠 Tech Stack

| Category | Tools & Technologies |
|--------|----------------------|
| **Cloud Provider** | AWS |
| **Storage (Data Lake)** | Amazon S3 (Bronze, Silver, Gold layers) |
| **ETL / Processing** | AWS Glue, Apache Spark (PySpark) |
| **Data Validation** | Amazon Athena |
| **Analytics / Warehousing** | Amazon Redshift |
| **Programming Language** | Python, PySpark |
| **Architecture Pattern** | Bronze–Silver–Gold Lakehouse Architecture |
| **Data Format** | CSV |
| **Use Case** | Batch Data Processing & Analytics |


## 🏗️ Architecture Diagram (Bronze → Silver → Gold)

The following diagram illustrates the end-to-end AWS data pipeline following the **Bronze–Silver–Gold lakehouse architecture**.

![ETL Pipeline Architecture](architecture/etl-pipeline-architecture.png)

### Architecture Flow
1. **Bronze Layer (Amazon S3)**
Raw COVID data is ingested in CSV format and stored as the immutable source of truth.

2. **Silver Layer (AWS Glue + PySpark)**
Raw data is cleaned, standardized, and converted to Parquet format for optimized processing.

3. **Gold Layer (AWS Glue + PySpark)**
Business logic and aggregations are applied to create analytics-ready datasets.

4. **Validation (Amazon Athena)**
SQL queries are used to validate schema, record counts, and data correctness.

5. **Analytics (Amazon Redshift)**
Curated Gold data is queried for analytical insights and reporting.

---

## 📸 Pipeline Execution & Validation



---





This section showcases the end-to-end execution of the AWS Bronze–Silver–Gold pipeline, covering ETL processing, validation, storage layout, and analytics.

<table width="100%"> <tr> <td align="center" width="50%"> <img src="screensots/glue-job-sucess.png" width="95%" alt="AWS Glue ETL Job Success"/> </td> <td align="center" width="50%"> <img src="screensots/athena-validation.png" width="95%" alt="Amazon Athena Data Validation"/> </td> </tr> <tr> <td align="left"> <b style="font-size:18px;">AWS Glue ETL Job Success</b> </td> <td align="right"> <b style="font-size:18px;">Amazon Athena Data Validation</b> </td> </tr> <tr> <td align="left"> PySpark-based AWS Glue jobs successfully executed, transforming raw COVID data from the Bronze layer into cleaned and standardized Silver datasets. </td> <td align="right"> Athena SQL queries validate schema integrity, record counts, and data correctness before downstream analytics. </td> </tr> </table>
<br/> <table width="100%"> <tr> <td align="center" width="50%"> <img src="screensots/bron-sil-gol.jpg" width="95%" alt="S3 Bronze Silver Gold Layout"/> </td> <td align="center" width="50%"> <img src="screensots/redshift-query-results .png" width="95%" alt="Amazon Redshift Query Results"/> </td> </tr> <tr> <td align="left"> <b style="font-size:18px;">S3 Bronze–Silver–Gold Lakehouse Layout</b> </td> <td align="right"> <b style="font-size:18px;">Amazon Redshift Analytics Results</b> </td> </tr> <tr> <td align="left"> Clearly defined S3 folder structure separating raw, cleaned, and curated datasets following lakehouse best practices. </td> <td align="right"> Analytical SQL queries executed in Amazon Redshift on Gold-layer data to generate insights and reporting. </td> </tr> </table>
