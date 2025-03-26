# data-analyst-meet
# Project Title: Data Quality Control Implementation for City of Vancouver Open Data Using AWS Glue
# Project Description:
This project implements a robust Data Quality Control (DQC) pipeline for open datasets provided by the City of Vancouver, using AWS Glue for automated ETL, validation, and schema monitoring. The pipeline ensures high-quality datasets by detecting and correcting data issues and separating valid and invalid records. The main dataset used was business license data, and the workflow was visualised using draw.io.
# Objective:
To build an end-to-end data quality control framework on AWS that automates profiling, validation, and monitoring of public datasets—enhancing reliability for downstream analytics and improving civic transparency.
# Background:
The City of Vancouver offers open datasets including business licenses, property data, traffic, and public service records. However, many datasets contain inconsistent formats, missing values, and schema drift over time. A DQC process was implemented using AWS Glue’s Visual ETL flow, S3 buckets, and conditional logic routing to enable reliable public analytics.
# Dataset Used:
  •	File: business-licences.csv
  •	Source: City of Vancouver Open Data
  •	Fields: Business ID, Category, Licence Date, Status, Location, etc.
# Methodology:
1.	Data Ingestion: 
  •	Ingested raw CSV into Amazon S3(Van-ani-trf-meet bucket).
2.	Data Quality Evaluation: 
  •	Created a Visual ETL job in AWS Glue titled van-ani-QC-meet.
  •	Used “Evaluate Data Quality” transform.
  •	Applied schema and logical rules fields like status, licence number and extract date.
![AWS Analysis Pipeline](https://github.com/Meet1234-cmd/data-analyst-meet/blob/main/prj2S12.png)
3.	Conditional Routing:
  •	Used “Conditional Router” to classify records as passed or failed based on the rule success.
4.	Data Handling:
  •	Valid records stored in Quality_Check/Passed/
![AWS S3 folder displaying vaild Records](https://github.com/Meet1234-cmd/data-analyst-meet/blob/main/prj2S13.png)
  •	Invalid records stored in Quality_Check/Failed/
![AWS S3 folder displaying Invaild Records](https://github.com/Meet1234-cmd/data-analyst-meet/blob/main/prj2S14.png)
6.	Schema Alignment:
  •	Applied change schema transformation before loading
7.	Output:
  •	Used S3 buckets to store the cleaned and invalid datasets separately for transparency and future auditability.
8.	Architecture Design:
  •	Data pipeline architecture was documented using draw.io.
# AWS Services Used:
- AWS Service    - Purpose
  -S3	             -Raw + Processed Data Storage
  -Glue Studio	   -Visual ETL + Data Quality Control Logic
  -Glue Jobs 	     -Schema transformation + Conditional routing
  -Draw.io	       -Visualizing architecture and data flow
# Deliverables:
  •	AWS Glue visual ETL pipeline for schema validation
  •	Split logic for valid/invalid record routing
  •	Clean dataset for further analytics
  •	Architecture diagram of pipeline
  •	S3-stored record output separation
  •	Visual documentation via screenshots
# TimeLine:
- Phase	                    - Duration
-Data Analysis	              -1 Week
-AWS Glue Pipeline Setup	    -2 Weeks
-Quality Rule Creation	      -1 Week
-Validation & Output	        -1 Week
-Documentation & Upload	      -1 Week




