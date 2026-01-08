<div align="center"> <h1>🌸 Global Green Energy Transition Tracker</h1> <h3><span style="color:#ff4da6;">Azure Cloud End to End Data Engineering Pipeline</span></h3> <p> A cloud native, end to end data engineering project for tracking global renewable energy trends built to ingest, process, and visualize <strong>30,000+ power plants</strong> alongside <strong>100+ years</strong> of historical energy metrics. </p> </div>


<img width="1152" height="641" alt="e3ea415b-1544-4458-b035-1c8907c78b66" src="https://github.com/user-attachments/assets/77a5c4b6-ddf3-4908-ac0c-b2b6de04e095" />


🎀 Project Overview


This project is a full E2E Azure pipeline that turns raw energy datasets into a clean analytics layer and an interactive Power BI dashboard.
It follows a scalable design pattern and focuses on data quality, lineage, and fast BI reporting.

💗 Architecture (Medallion: Bronze → Silver → Gold)

🍒 Bronze : Ingestion

Azure Data Factory (ADF) orchestrates ingestion and moves raw data into Azure Data Lake Storage (ADLS) Gen2.

Goal: keep data as is, traceable, and easy to reprocess.

🌷 Silver : Transformation

Azure Databricks (PySpark) cleans and standardizes data:

null handling

schema enforcement

consistent formatting

Output is stored in Parquet for efficient downstream processing.

💓 Gold : Serving

Curated data is loaded into Azure SQL Database via JDBC.

Designed as the main serving layer with a relational schema optimized for analytics and reporting.

🎀 Visualization

Power BI Desktop connects to the Gold layer to deliver:

geospatial exploration

time-series trend analysis

interactive filtering across views

🌸 Tech Stack

Cloud: Microsoft Azure

Orchestration: Azure Data Factory (ADF)

Storage: ADLS Gen2

Compute: Azure Databricks (Apache Spark / PySpark)

Database: Azure SQL Database

BI: Power BI Desktop

💖 Key Features

Geospatial Analytics: Interactive global map of power plants by fuel type (Solar, Wind, Hydro, Coal, Gas, …)

Cross Filtering: Bidirectional relationships enabling dynamic slicing by region, emissions, and energy trends

Enterprise style Pipeline: Distributed Spark processing + optimized formats for large datasets

🌷 Setup & Implementation

Provision Infrastructure

ADLS Gen2, Databricks Workspace, Azure SQL Server/DB

Configure Security

Firewall rules, managed identities, and service to service access

Run Transformations

Import PySpark notebooks into Databricks and execute the pipeline

Initialize Database Schema

Run SQL DDL scripts in sql_scripts/ to create Fact + Dimension tables

Open Power BI Report

Open the .pbix file and update connection parameters to your Azure SQL instance

🧠 Technical Competencies Demonstrated

Cloud Security: Firewall configuration + authentication for secure service communication

Storage Optimization: Parquet columnar storage for faster queries and smaller footprints

Data Modeling: Analytical star-schema design to support complex slicing in BI tools
