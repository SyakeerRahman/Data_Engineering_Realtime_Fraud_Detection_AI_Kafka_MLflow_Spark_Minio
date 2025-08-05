# Data_Engineering_Realtime_Fraud_Detection_AI_Kafka_MLflow_Spark_Minio

Realtime Fraud Detection AI Data Pipeline Data Engineering Project | Data Pipeline using Kafka, Pyspark, MLflow

I want to share my latest Data Engineering project where I put my skills to the test by working with an AWS cloud

🔬𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗢𝘃𝗲𝗿𝘃𝗶𝗲𝘄: This project provides a comprehensive data pipeline solution to extract, transform, and load (ETL) Reddit data into a Redshift data warehouse. The pipeline leverages a combination of tools and services including Apache Airflow, Celery, PostgreSQL, Amazon S3, AWS Glue, Amazon Athena, and Amazon Redshift.

💾 𝗗𝗮𝘁𝗮 𝗦𝗼𝘂𝗿𝗰𝗲:

🎯 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗚𝗼𝗮𝗹𝘀:

Extract data from Reddit using its API.
Store the raw data into an S3 bucket from Airflow.
Transform the data using AWS Glue and Amazon Athena.
Load the transformed data into Amazon Redshift for analytics and querying.

🔧The tools that are covered in this project are:

Reddit API: Source of the data.
Apache Airflow & Celery: Orchestrates the ETL process and manages task distribution.
PostgreSQL: Temporary storage and metadata management.
Amazon S3: Raw data storage.
AWS Glue: Data cataloging and ETL jobs.
Amazon Athena: SQL-based data transformation.
Amazon Redshift: Data warehousing and analytics.


## Prerequisites

1. High Level Architecture Walkthrough
2. System Requirements
3. Tools used and why
4. Machine Learning Features Walkthrough
### 5. Setting up the Architecture

- `python -m venv venv`
- `.\venv\Scripts\Activate.ps1`
- `docker-compose.yaml`
- `mkdir airflow > Dockerfile + requirements.txt`
- `mkdir mlflow > Dockerfile + requirements.txt`
- `touch wait-for-it.sh`
- `touch .env`
- `docker compose --profile flower up -d --build`
- `docker compose --profile flower down (to stop container) - if needed`
- `docker compose down -v (remove volume) - if needed`
- `make sure all server working`
  
<img width="1886" height="919" alt="image" src="https://github.com/user-attachments/assets/fc828a2a-6083-42e5-a585-2634efe10ca5" />
<img width="1892" height="702" alt="image" src="https://github.com/user-attachments/assets/e7c1841e-a117-4dc7-a611-d57e5623bc15" />
<img width="1883" height="616" alt="image" src="https://github.com/user-attachments/assets/4faa4486-cddf-4a9e-a68b-5796f44f914e" />
<img width="1872" height="989" alt="image" src="https://github.com/user-attachments/assets/318ae46d-3769-4ba1-ac7d-bfcbc4361d54" />

if minio have no bucket 
- chmod +x wait-for-it.sh
- compose down minio
- compose down mc
- compose up mc build -d --build

### 6. Financial Transactions Producer

- mkdir producer > Dockerfile + requirements.txt + main.py
- pip install -r producer/requirements.txt


8. Creating High Throughput and High Performance Kafka Cluster
9. Training Fraud Detection Model
10. Machine Learning Features Implementation
11. Reviewing Generated Model and Promoting them to Production
12. Realtime Inference with Apache Spark
13. Review Fraud Transactions Inference Results
