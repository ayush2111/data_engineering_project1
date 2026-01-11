# Full Load API ETL Pipeline 

## 📌 Project Overview
This project implements an **end-to-end full load ETL pipeline** to ingest raw data from multiple **GitHub REST API sources**, perform transformations using **Databricks (PySpark)**, and deliver **clean, analytics-ready tables** for reporting and analysis.

The pipeline is built using a **lookup-driven, metadata-based architecture** and follows **Bronze–Silver data lake best practices** to ensure scalability, reusability, and data traceability.

---

## 📸 Azure Data Factory Pipeline

The diagram below represents the **ADF pipeline orchestration** used for full-load ingestion from GitHub APIs.

It demonstrates:
- Lookup-driven metadata processing
- Dynamic ForEach iteration over multiple source tables
- Parameterized and reusable copy activities

![ADF Pipeline](https://github.com/ayush2111/data_engineering_project1/blob/main/Screenshot%202026-01-11%20161824.png)

---

## 📂 Data Sources
- Ingested raw data from **GitHub API source tables**
- **Full load strategy** implemented for all source tables

---

## 🔄 ETL Workflow

### 1️⃣ Ingestion – Full Load (ADF)
- Designed a **full-load ingestion framework** using Azure Data Factory.
- Created a **lookup table** to store:
  - Source table name
  - GitHub API endpoint
  - Target storage path
- Used **Lookup + ForEach activities** to dynamically iterate over source tables.
- Implemented **Copy activities** to extract data from GitHub APIs.
- Stored raw data in the **Bronze layer** without transformations.

---

### 2️⃣ Transformation – Silver Layer (Databricks)
- Developed **Databricks PySpark notebooks** for Silver-layer transformations:
  - Data cleansing and standardization
  - Handling null values and invalid records
  - Schema alignment and data type casting
  - Deduplication logic

---

### 3️⃣ Clean / Analytics Tables
- Created **clean, analytics-ready tables** from Silver-layer data.
- Optimized tables for:
  - Reporting
  - BI dashboards
  - Downstream analytics use cases
- Ensured consistency, quality, and usability of data.

---

## ✅ Key Features
- Full-load ETL design
- Lookup-driven, metadata-based ingestion
- Scalable ForEach orchestration
- Bronze–Silver data architecture
- Clean, analytics-ready outputs
- Reusable and parameterized pipelines

---
