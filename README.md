# Tigray Genocide Data Pipeline

This project involves building a data pipeline to manage and process over 1TB of data on genocide victims in Tigray, including their names and exact coordinates.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tigray-genocide-data-pipeline.git
   cd tigray-genocide-data-pipeline
pip install -r requirements.txt
python src/ingestion.py
python src/processing.py
apache-spark
apache-airflow
tensorflow
nvidia-cuda-toolkit
pandas
geopandas
# src/ingestion.py

import pandas as pd
from pyspark.sql import SparkSession

def ingest_data(file_path):
    spark = SparkSession.builder.appName("TigrayDataIngestion").getOrCreate()
    df = spark.read.csv(file_path, header=True, inferSchema=True)
    df.write.format("parquet").save("data/raw/")
version: '3'
services:
  spark:
    image: bitnami/spark:latest
    ports:
      - "8080:8080"
    environment:
      - SPARK_MODE=master
  airflow:
    image: apache/airflow:latest
    ports:
      - "8081:8080"
    environment:
      - AIRFLOW__CORE__LOAD_EXAMPLES=False
git add .
git commit -m "Initial commit with project structure and setup"
git push origin main
