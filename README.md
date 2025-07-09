# Real-Time Stock Market Data Engineering Project using Kafka & AWS

##  Project Overview

This project demonstrates an **End-to-End Data Engineering Pipeline** for processing **real-time stock market data**. It focuses on how to build scalable and cloud-based data pipelines using **Apache Kafka** and **AWS services**.

Our main goal is to understand the operational aspects of a Data Engineering workflow—streaming data ingestion, transformation, and querying.

---

## Technologies Used

- **Programming Language**: Python
- **Streaming Platform**: Apache Kafka
- **Cloud Platform**: Amazon Web Services (AWS)
  - **S3 (Simple Storage Service)** – Data lake storage
  - **AWS Glue** – Metadata catalog and ETL
    - Glue Crawler
    - Glue Catalog
  - **Amazon Athena** – SQL-based querying on S3 data
  - **EC2** – Kafka producer/consumer hosting

---

##  Dataset

You can use any stock market dataset that suits your use case.  
For this project, we used the following CSV dataset:

📁 [indexProcessed.csv](https://github.com/darshilparmar/stock-market-kafka-data-engineering-project/blob/main/indexProcessed.csv)

---

##  Project Workflow

1. **Kafka Producer**  
   - Reads data from CSV file.
   - Sends data to a Kafka topic in real-time (or simulated real-time).

2. **Kafka Consumer (Optional)**  
   - Reads messages from the Kafka topic (for testing/logging).

3. **EC2 Instance**  
   - Used to run Kafka Broker, Producer, and Consumer scripts.

4. **AWS S3**  
   - Consumer writes the streamed data to an S3 bucket as CSV/JSON files.

5. **Glue Crawler & Catalog**  
   - Automatically detects schema and updates Glue Data Catalog.

6. **Amazon Athena**  
   - Queries the data stored in S3 using SQL.

---

##  Key Concepts

- Kafka streaming in real-time (or simulated)
- Writing streaming data to AWS S3
- Automated schema detection with Glue Crawlers
- Querying large datasets with Athena using SQL

---

##  Notes

- Ensure Kafka is properly set up on your EC2 instance.
- Set up correct IAM roles for Glue and Athena to access S3.
- This project focuses more on the **operational and orchestration** aspects than ML/data analysis.
