# TCS_data_engineering_project_1

## This project demonstrates how data flows from various source systems to a data warehouse and is then used to generate insightful dashboards and reports. 

## 1. Data Flow:
![Data flow](https://github.com/user-attachments/assets/eb7102e4-4e1b-4a4e-a9af-b32b06c6be95)

  This shows how data is gathered from multiple sources, processed, and used for creating reports and dashboards:
  
  Sources: Data comes from different systems (e.g., databases and external applications).
  Informatica: This is a tool that acts as a bridge. It extracts the data, cleans it up, and loads it into the data warehouse.
    Full Load: Loads all the data.
    Incremental Load: Only updates the new or changed data.
  PostgreSQL Data Warehouse: A database where the cleaned and processed data is stored and organized for analysis.
  Dashboards and Reports: Tools like Qlik Sense and Excel are used to create visualizations and reports, helping teams make decisions based on the processed data.
  
## 2. ETL Process:
![ETL](https://github.com/user-attachments/assets/89e556b2-e2cb-4db1-bcb4-8112b707107c)

  This explains how data is loaded into the system:
  
  Full Load:
    The entire table is refreshed by deleting old data and inserting new data (also called "Truncate and Insert").
    
  Incremental Load: 
  Only the new or updated records are processed.
    Without Primary Key: Uses parameters like start and end dates to identify changes.
    With Primary Key: Uses advanced techniques like "Lookup" and "Update" to identify and process changes.

## 3. Data Warehouse Structure:
![schema](https://github.com/user-attachments/assets/fa870869-8b7f-4953-890e-3a59aaddb92f)

  This shows the structure of the data warehouse and how data is organized step-by-step:

  Staging (Stg Schema): Temporary storage where raw data from sources is first loaded.
  
  Dimension (Dim Schema): Stores Master data. This information doesn't change often but is critical for understanding data.
  
  Fact (Fact Schema): Stores transactional data (in denormalized form) used for reporting and analysis.
  
  Temporary (Tmp Schema): Used for intermediate calculations or transformations.
  
  Report (Rpt Schema): The final step where processed data is ready for reporting and dashboards.
