# Weather Data Engineering Pipeline
An end-to-end data engineering pipeline that ingests weather data from an API, stores raw data in a data lake, and transforms nested JSON into a structured dataset using PySpark.

## Problem Statement
How can we ingest weather data from an API and convert nested JSON into an analytics-ready dataset?

## Architecture
OpenWeather API  
↓  
Azure Data Factory  
↓  
Azure Data Lake Storage (Bronze Layer – Raw JSON)  
↓  
Azure Databricks (PySpark Processing)  
↓  
Silver Dataset (Delta Table)

## Tech Stack
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- Apache Spark (PySpark)
- Delta Lake
- OpenWeather API

## Pipeline Flow
1. Azure Data Factory calls the OpenWeather API
2. Raw JSON files are stored in Azure Data Lake (Bronze layer)
3. Azure Databricks reads the JSON files
4. PySpark flattens the nested structure
5. Clean dataset is written as a Delta table (Silver layer)

## Example Output Dataset
| city | temperature | humidity | weather_condition |
|-----|-----|-----|-----|
| Mumbai | 31 | 70 | Clouds |
| Delhi | 29 | 65 | Clear |
| Pune | 28 | 69 | Haze |
