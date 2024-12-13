# Youtube-Data-Pipeline-using-AWS
This project contains an end-to-end data pipeline built to analyze trending YouTube videos using a combination of AWS services. The project utilizes the Kaggle dataset of trending YouTube videos and demonstrates the integration of various AWS tools to process, analyze, and visualize the data.

# Dataset Description
This dataset is from Kaggle collected using the Youtube API.This dataset is a daily record of the top trending YouTube videos.It includes several months of data on daily trending YouTube videos. Data is included for the US, GB, DE, CA, and FR regions (USA, Great Britain, Germany, Canada, and France, respectively), with up to 200 listed trending videos per day.

# Project Goals:
Data Ingestion — Develop a system to efficiently ingest data from multiple sources.

ETL Process — Since the data is received in raw form, we will transform it into a structured, usable format.

Data Lake — Implement a centralized repository to store and manage data from various sources.

Scalability — Ensure that the system can scale effectively as data volume grows over time.

Cloud Infrastructure — Leverage cloud resources, specifically AWS, to handle large datasets that exceed local processing capabilities.

Reporting — Create an interactive dashboard to provide insights and answer the key questions posed earlier.

# AWS Services Used
Amazon S3 (Simple Storage Service): A scalable object storage service used to store raw data, intermediate results, and processed outputs securely in the data pipeline. I used S3 buckets to first store the raw data(csv and json format) using the AWS Command Line Interface. Then usde S3 buckets to store cleansed data to use for further processing.

AWS Glue: A fully managed ETL (Extract, Transform, Load) service that automates the process of cleaning, transforming, and preparing the raw data for analysis. It also creates a data catalog for easy querying. Made use of Crawlers to build data catalogs. Also used glue studio to perform ETL jobs to transform data and export cleaned to reporting layer.

Amazon Athena: A serverless interactive query service that allows SQL-based querying of data stored in S3 without the need for complex data infrastructure management. Used Athena to query data and also identify the errors faced in the structure of the data.

AWS Lambda: A serverless compute service that automates data processing tasks and orchestration, such as triggering ETL jobs, without the need to manage servers.

AWS IAM (Identity and Access Management): Ensures secure access management, controlling who has permission to access and manage the AWS resources used in the pipeline. Attached IAM roles to the other services used to allow them access to the required services.

Amazon QuickSight: A business intelligence and visualization tool that enables the creation of interactive dashboards, allowing insights and trends from the processed data to be easily visualized and analyzed. Visualized the clean dataset to uncover key insights.

# Architecture
https://github.com/anushkauniyal20/Youtube-Data-Pipeline-using-AWS/blob/main/architecture.jpeg
