# End To End ETL Pipeline On Travel&Trip (Databricks + PySpark)

## 📌 Overview

This project builds a scalable end-to-end data pipeline to process e-commerce transactional data and generate business-critical insights such as revenue trends, customer behavior, and product performance.

The pipeline follows a medallion architecture (Bronze, Silver, Gold) and is implemented using PySpark and SQL on Databricks, with AWS S3 as the storage layer.

## 🎯 Business Problem

Raw transactional data from multiple sources is often inconsistent, duplicated, and not suitable for analytics. This project transforms raw data into clean, structured, and aggregated datasets to support reporting and decision-making.

## 🚀 Features

* Ingestion of raw order, customer, and product data into Bronze layer
* Data cleaning, deduplication, and validation in Silver layer
* Business-level aggregations in Gold layer
* Scalable processing using distributed PySpark jobs
* Structured pipeline aligned with real-world data engineering practices

## 🛠️ Tech Stack

* PySpark
* SQL
* Databricks
* AWS S3

## 🧱 Architecture

### Bronze Layer

* Raw ingestion from source (CSV/JSON)
* Schema-on-read approach
* No transformations applied

### Silver Layer

* Data cleaning (null handling, type casting)
* Deduplication using business keys
* Joining datasets (orders + customers + products)

### Gold Layer

* Aggregated datasets for analytics:

  * Daily revenue
  * Top-selling products
  * Customer lifetime value (CLV)
  * Order trends

## 📊 Key Metrics Generated

* Total Revenue per Day
* Average Order Value (AOV)
* Top 10 Products by Sales
* Customer Retention Insights

## 📂 Project Structure

```id="k2m9zp"
.
├── data/
│   ├── bronze/
│   ├── silver/
│   └── gold/
├── notebooks/
│   ├── bronze_ingestion
│   ├── silver_transformation
│   └── gold_aggregation
├── scripts/
│   ├── bronze_etl.py
│   ├── silver_etl.py
│   └── gold_etl.py
└── README.md
```

## ⚙️ Setup Instructions

1. Clone the repository:

```bash id="z7d2lo"
git clone https://github.com/your-username/ecommerce-etl-pipeline.git
cd ecommerce-etl-pipeline
```

2. Upload notebooks/scripts to Databricks

3. Configure AWS S3 access:

* Create S3 bucket
* Configure IAM role or access keys
* Mount S3 to Databricks

4. Execute pipeline:

* Run Bronze ingestion
* Run Silver transformation
* Run Gold aggregation

## ▶️ Usage

* Load raw e-commerce datasets into S3
* Execute pipeline in sequence
* Query Gold layer for analytics insights

## 📸 Screenshots

* Databricks job execution
* Sample query results
* Dashboard (if connected)

## 🧪 Data Quality Checks

* Null validation
* Duplicate removal
* Schema enforcement

## 🚧 Future Improvements

* Workflow orchestration using Apache Airflow
* Incremental data processing
* Real-time streaming pipeline
* Integration with BI tools (Power BI / Tableau)
