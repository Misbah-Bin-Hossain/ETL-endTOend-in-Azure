
# ETL Project: Football Data Analytics

This project implements an end-to-end ETL (Extract, Transform, Load) pipeline to analyze football data. The pipeline extracts data from a football API, processes it using Azure Data Factory and Databricks, loads it into SQL Server, and visualizes the insights in Power BI.

## Project Workflow

![Diagram](https://github.com/user-attachments/assets/3399d4ae-8924-4b10-bfcb-4e2ef53721b8)


1. **Data Extraction**
   - Extracted data from a football API using Azure Data Factory.
   - Configured dynamic pipelines to handle different parameters (e.g., league, season, filter type).
   - Stored API responses as Parquet files in Azure Blob Storage.

2. **Data Transformation**
   - Processed the data in Databricks through two notebooks:
     - **Bronze to Silver**: Cleaned and normalized raw API data.
     - **Silver to Gold**: Performed advanced transformations and created analysis-ready datasets.

3. **Data Loading**
   - Loaded the processed data into a SQL Server database using JDBC connections from Databricks.

4. **Data Visualization**
   - Designed a Power BI dashboard with the following insights:
     - Team standings
     - Match results
     - Top scorers and player statistics
     - Squad details

## Tools & Technologies

- **Azure Data Factory**: For orchestrating the ETL pipeline.
- **Azure Databricks**: For data transformation using PySpark.
- **Azure Blob Storage**: For storing raw and intermediate data.
- **SQL Server**: As the target database for transformed data.
- **Power BI**: For creating interactive dashboards.

## Folder Structure

```
- notebooks/
    - Bronze_to_Silver.ipynb  # Initial cleaning and normalization
    - Silver_to_Gold.ipynb    # Advanced transformations
- data_factory/
    - AzureDataFactory.json   # Azure Data Factory pipeline configuration
- power_bi/
    - Dashboard.pptx          # Power BI dashboard screenshots
```

## How to Run

1. Set up Azure Data Factory and configure the provided pipeline JSON file.
2. Deploy Databricks notebooks (`Bronze_to_Silver` and `Silver_to_Gold`) and connect to your Azure Blob Storage and SQL Server.
3. Run the pipeline to fetch and process data.
4. Load the transformed data into SQL Server.
5. Import the data into Power BI to visualize the insights.

## Key Features

- Dynamic pipeline configuration for fetching data across multiple seasons and leagues.
- Rate-limit handling for API calls using Wait activities in Azure Data Factory.
- Comprehensive data cleaning and transformation in Databricks.
- Real-time refreshable Power BI dashboard.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Thanks to the football API provider for making the data accessible.
- Gratitude to Microsoft Azure for their powerful tools enabling this project.

---
For any questions or feedback, feel free to contact me via GitHub Issues.

Few Examples of my dashboard:

<img width="567" alt="{9F9AEED4-30C4-4872-97A2-B9DC43BB04D3}" src="https://github.com/user-attachments/assets/0c34bdee-d42e-458a-a3a3-14c11379d2ef">

<img width="566" alt="{20E0D79F-4111-4A0E-B035-95B5E89DA5E8}" src="https://github.com/user-attachments/assets/dc9f83bf-6d95-483e-badf-6bad8503492d">

<img width="601" alt="{4313CDBC-F6C8-46C5-B9B8-A62329A9ACC5}" src="https://github.com/user-attachments/assets/c921e9dc-c756-4cad-ae38-8d8df16005aa">

<img width="601" alt="{25DC5AE1-D545-4746-9EAB-DE91347DB05F}" src="https://github.com/user-attachments/assets/0fe79df6-2c4d-4c1b-9e3c-14c6eb312964">




