# 🚀 AWS Bronze–Silver–Gold COVID Data Pipeline

An end-to-end **AWS Data Engineering pipeline** implementing the **Bronze → Silver → Gold** architecture using **Amazon S3, AWS Glue (PySpark), Athena, and Amazon Redshift** to ingest, transform, validate, and analyze COVID-19 data at scale.

---

## 📌 Project Overview

This project demonstrates a real-world cloud data pipeline following modern **data lakehouse best practices**.  
Raw COVID data is ingested into S3, transformed using scalable PySpark jobs in AWS Glue, validated with Athena, and finally queried in Amazon Redshift for analytics.

The pipeline is fully automated and production-style.

---

## 🏗️ Architecture (Bronze → Silver → Gold)

``` mermaid
flowchart LR
    A[Raw COVID Data Source]
    B[Amazon S3 - Bronze Layer]
    C[AWS Glue ETL - PySpark<br/>Bronze to Silver]
    D[Amazon S3 - Silver Layer<br/>Cleaned and Standardized]
    E[AWS Glue ETL - PySpark<br/>Silver to Gold]
    F[Amazon S3 - Gold Layer<br/>Analytics Ready]
    G[Amazon Athena<br/>Data Validation]
    H[Amazon Redshift<br/>Analytics and Reporting]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H


