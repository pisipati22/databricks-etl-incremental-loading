Databricks ETL Pipeline with Incremental Loading, Data Warehousing, and SCD Type 1

This project showcases an end-to-end ETL + Data Warehousing pipeline built in Databricks (PySpark + Delta Lake). 
The pipeline includes:

- Incremental Data Loading
- ETL Pipeline → Staging → Transformation → Core Layer
- Dimensional Data Modeling (Fact & Dimension Tables)
- SCD Type 1 updates
- Star Schema Design
- Delta Lake MERGE logic

Project Architecture:
Source Data → Staging Layer → Transformation Layer → Core Layer (Fact + Dimension Tables) → Incremental Load → Analytics

Data Warehousing Layers:
1. Staging Layer – Raw data, no transformations
2. Transformation Layer – Cleaning, standardizing, business rules
3. Core Layer – Final fact & dimension tables 

Dimensional Modeling:
- Fact tables store numeric metrics (e.g., FactSales)
- Dimension tables store descriptive attributes (DimCustomer, DimProduct, DimDate)
- Star Schema: Fact table in center connected to dimension tables

Incremental Loading:
- Processes only new/updated data
- Uses Delta Lake MERGE INTO
- Timestamp or key-based logic

SCD Type 1:
- Overwrites existing values
- Does not maintain historical changes
- Always keeps latest information

Repository Structure:
notebooks/
data/
diagrams/
README.md

Technologies Used:
Databricks, PySpark, Delta Lake, SQL, Data Warehousing, Star Schema, SCD Type 1, Incremental Loading
