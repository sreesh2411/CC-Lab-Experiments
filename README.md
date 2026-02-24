# Cloud Computing Laboratory (UE18CS354) Experiments

## Overview
This repository contains the files, source code, and outputs for the assignments and experiments conducted as part of the **Cloud Computing Laboratory (UE18CS354)** course. 

The experiments explore practical cloud infrastructure management, containerization, orchestration, and big data processing in the cloud.

## 🛠️ Tech Stack & Tools
* **Cloud Provider:** Amazon Web Services (AWS) - EC2, S3, VPC, EMR
* **Containerization & Orchestration:** Docker, Docker Compose, Kubernetes
* **CI/CD:** Jenkins
* **Big Data Processing:** Apache Spark (PySpark)
* **Languages:** Python, C, HTML

## 📂 Repository Structure
The repository is organized sequentially by weeks, containing source code, configuration files (YAML, Dockerfiles), and execution screenshots verifying the outputs.

* **Week 1 - 4: AWS Infrastructure Basics**
  * Configuring Virtual Private Clouds (VPCs), subnets, and routing.
  * Deploying EC2 instances and associating Elastic IPs.
  * Modifying inbound security group rules.
  * Interacting with Amazon S3 buckets.
  * Deploying basic Python applications (`application.py`, `requirements.txt`).
* **Week 5 & 7: Containerization with Docker**
  * Containerizing applications using custom `Dockerfile`s.
  * Managing multi-container environments using `docker-compose.yml`.
* **Week 8: Orchestration with Kubernetes**
  * Writing and applying Kubernetes manifests (`pod.yaml`, `deploy.yaml`, `deploy_service.yaml`).
  * Deploying scalable applications and services (e.g., Nginx) on Kubernetes clusters.
* **Week 9: Big Data Analytics in the Cloud**
  * Processing large datasets using Apache Spark (likely via AWS EMR).
  * Features `health_violations.py`, a PySpark script that queries food establishment inspection data to find the top 10 establishments with the most 'RED' violations.
* **Week 10 - 11: CI/CD & Advanced Cloud Concepts**
  * Implementation of continuous integration and delivery pipelines using Jenkins.
  * Additional cloud configurations and testing.

## 🚀 Highlight: PySpark Health Violations Analysis (Week 9)
A key experiment demonstrating data processing at scale. The `health_violations.py` script utilizes Spark SQL to aggregate and analyze CSV data from Amazon S3. 

**Execution Example:**
```bash
spark-submit health_violations.py \
    --data_source s3://YOUR-BUCKET/food_establishment_data.csv \
    --output_uri s3://YOUR-BUCKET/restaurant_violation_results
