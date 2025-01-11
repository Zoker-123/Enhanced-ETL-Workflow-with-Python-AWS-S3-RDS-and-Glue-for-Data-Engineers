# Enhanced-ETL-Workflow-with-Python-AWS-S3-RDS-and-Glue-for-Data-Engineers

## Project Overview
This extended project aims to integrate AWS services into a robust ETL (Extract, Transform, Load) pipeline. The project involves extracting data from CSV, JSON, and XML files, transforming the data (e.g., performing unit conversions), and loading it into AWS S3 and AWS RDS for further use. AWS Glue can optionally be utilized for automating schema inference and transformations, further enhancing the pipeline.

## Technologies Used
* Python Data Formats: CSV, JSON, XML
* AWS Services: S3, RDS, Glue
* SQL

## Objectives
* Extract data from CSV, JSON, and XML files.
* Transform the extracted data, including unit conversions.
* Load transformed data into AWS S3 and AWS RDS.
* Optionally, automate parts of the ETL process using AWS Glue.
* Implement logging to monitor the ETL process.

## Dataset
* Download the dataset using the following command:
-> wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0221EN-SkillsNetwork/labs/module%206/Lab%20-%20Extract%20Transform%20Load/data/source.zip

* Unzip the file:
-> unzip source.zip -d ./unzipped_folder

The folder will contain CSV, JSON, and XML files for processing.

## Project Steps
-> Step 1: Gather Data Files
* Download and unzip the dataset to obtain multiple file formats.
* Verify the presence of CSV, JSON, and XML files in the project folder.

-> Step 2: AWS Setup
* Create an S3 Bucket:
- Store raw and transformed data files in this bucket.

* Set Up AWS RDS:
- Create a MySQL or PostgreSQL RDS instance.
- Configure security groups to allow access from your local machine or Lambda functions.

* Set Up AWS Glue:
- Create a Glue crawler to detect schema and manage ETL jobs.

-> Step 3: Import Libraries and Configure AWS Resources
* Required Libraries:
- boto3: Interact with AWS S3 and RDS.
- pandas: Data manipulation.
- sqlalchemy: Connect to RDS databases.

* Set up AWS credentials in environment variables or AWS config files for secure access.

-> Step 4: Define Functions for ETL with AWS Integration
* Extract Data:
- Upload raw files to S3.
- Download raw files from S3 for processing.

* Transform Data:
- Perform unit conversions (e.g., inches to meters, pounds to kilograms).
- Clean and standardize data.

* Load Data to AWS:
- Store transformed data in S3 as transformed_data.csv.
- Load data into an RDS table using SQLAlchemy and pandas.

* Automate with AWS Glue:
- Use Glue for transformation and schema detection.

-> Step 5: Logging
* Use Python’s logging library to track each ETL phase.
* Save logs in a local file or upload them to S3 for centralized storage.

-> Step 6: Execution
* Upload Raw Data to S3:
- Extract and upload files to the S3 bucket.

* Extract and Transform Data:
- Download raw files from S3.
- Apply transformations and save locally or directly to S3.

* Load Data into AWS Services:
- Upload transformed CSV to S3.
- Load transformed data into RDS.

* Monitor Logs:
- Ensure logs capture the entire pipeline execution.

## Conclusion:

This project integrates AWS services to simulate a realistic cloud-based ETL workflow. Data engineers benefit from the scalability, monitoring, and automation provided by AWS. Proper logging ensures traceability, simplifying debugging and audits.
