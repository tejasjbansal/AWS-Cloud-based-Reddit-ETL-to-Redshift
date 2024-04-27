# AWS-Cloud-based-Reddit-ETL-to-Redshift

## Introduction

`AWS-Cloud-based-Reddit-ETL-to-Redshift` is a scalable and efficient data pipeline designed to extract, transform, and load (ETL) data from Reddit into an Amazon Redshift data warehouse. This project harnesses the power of cloud services and open-source tools to facilitate deep analytics on Reddit data, enabling insightful decision-making and strategic analysis.

## Features

- **Data Extraction**: Automatically pull data from Reddit using the Reddit API.
- **Data Storage**: Store raw data securely in Amazon S3 buckets.
- **Data Transformation**: Leverage AWS Glue and Amazon Athena for efficient data transformation.
- **Data Loading**: Load transformed data into Amazon Redshift for enhanced querying and analytics capabilities.
- **Automation and Orchestration**: Utilize Apache Airflow, backed by Celery, to manage and schedule the ETL pipeline tasks.
- **Scalability**: Easily scale resources up or down based on the processing needs.
- **Reliability**: Design to ensure high availability and fault tolerance of the ETL pipeline.

## Architecture

The architecture of this ETL pipeline encompasses several AWS services and tools, integrated to create a robust system for data processing:

![Blank diagram](https://github.com/tejasjbansal/AWS-Cloud-based-Reddit-ETL-to-Redshift/assets/56173595/71f11ce4-43a9-4d2e-a268-b14aa1455982)


1. **Reddit API**: Source endpoint for extracting data.
2. **Apache Airflow & Celery**: Orchestrate the entire ETL process and manage task execution across distributed systems.
3. **PostgreSQL**: Serve as a temporary storage and metadata management.
4. **Amazon S3**: Act as the primary storage for raw data before processing.
5. **AWS Glue**: Catalog raw data and manage transformation jobs.
6. **Amazon Athena**: Perform SQL-based transformations to prepare data for loading.
7. **Amazon Redshift**: Serve as the final data warehouse, where data is loaded and queried for insights.

## Getting Started

### Prerequisites

- AWS Account
- Access to Reddit API
- Apache Airflow setup
- PostgreSQL installation
- Familiarity with AWS services (Redshift, S3, Glue, Athena)

### Installation

1. **Set up your AWS environment**:
   - Create an S3 bucket for storing raw data.
   - Set up an Amazon Redshift cluster according to your data size and query performance requirements.
   - Configure AWS Glue for data cataloging and transformation jobs.
   - Set up Amazon Athena for querying transformed data.

2. **Configure Apache Airflow**:
   - Install Apache Airflow in your environment. Refer to the [official documentation](https://airflow.apache.org/docs/apache-airflow/stable/start.html) for installation guidance.
   - Configure Celery as the executor for better scalability and reliability.

3. **Deploy the Airflow DAGs**:
   - Clone this repository and place the DAG files into Airflow's DAGs folder.
   - Ensure that the Airflow scheduler and web server are up and running.

4. **Configure PostgreSQL**:
   - Set up a PostgreSQL database to manage metadata and temporary data during the ETL process.


## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change. Ensure to update tests as appropriate.
