# Flight Booking Data Pipeline with Airflow & CI/CD

A production-grade data engineering pipeline for processing flight booking data using PySpark, Google Cloud Platform, Apache Airflow, and CI/CD with GitHub Actions.

---

## Project Overview

This project demonstrates a scalable and automated data pipeline that processes raw flight booking data to generate meaningful business insights. It leverages PySpark on Dataproc Serverless for transformation, Airflow for orchestration, BigQuery for analytics storage, and GitHub Actions for CI/CD deployment across development and production environments.

---

## Tech Stack

- GitHub for source control
- GitHub Actions for CI/CD
- Google Cloud Storage (GCS) for data storage
- PySpark for data processing
- Dataproc Serverless for executing Spark jobs
- Apache Airflow for orchestration
- BigQuery for data warehousing and analytics

---

## Data Pipeline Workflow

```mermaid
graph TD
    A[Raw Flight Booking Data] -->|Upload to| B[Google Cloud Storage]
    B -->|Trigger Airflow DAG| C[Dataproc Serverless PySpark Job]
    C -->|Clean & Transform| D[Transformed Data]
    D -->|Load to| E[BigQuery Tables]
    E -->|Business Insights| F[Dashboard/Analytics]
