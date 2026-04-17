# Realtime Data Streaming | End-to-End Data Engineering Project

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [Technologies](#technologies)
- [Getting Started](#getting-started)

## Introduction

This project presents a complete end-to-end data engineering pipeline, designed to demonstrate how data flows from ingestion to processing and finally to storage in a real-world scenario.
It leverages a modern, scalable tech stack including Apache Airflow for orchestration, Apache Kafka and Apache Zookeeper for real-time streaming, Apache Spark for distributed data processing, and Apache Cassandra for high-performance data storage — all powered by Python.
The entire system is fully containerized using Docker, ensuring seamless deployment, scalability, and reproducibility.

## System Architecture

![System Architecture](https://github.com/airscholar/e2e-data-engineering/blob/main/Data%20engineering%20architecture.png)

The project is designed with the following components:

- **Data Source**: We use `randomuser.me` API to generate random user data for our pipeline.
- **Apache Airflow**: Responsible for orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.

## Technologies

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker
🐳 Docker Images

Pull all required images before running the project:

docker pull confluentinc/cp-zookeeper:7.4.0
docker pull confluentinc/cp-server:7.4.0
docker pull confluentinc/cp-schema-registry:7.4.0
docker pull confluentinc/cp-enterprise-control-center:7.4.0
docker pull apache/airflow:2.6.0-python3.9
docker pull postgres:14.0
docker pull bitnami/spark:latest
docker pull cassandra:latest


## Getting Started

1. Clone the repository:
    ```bash
    git clone https://github.com/muhammedshehab1995/Data-Engineering-Zoomcamp-Project.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Data-Engineering-Zoomcamp-Project
    ```

3. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up
    ```
