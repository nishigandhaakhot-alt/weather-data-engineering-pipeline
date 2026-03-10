# weather-data-engineering-pipeline

This project demonstrates a simple data engineering pipeline
that ingests weather data from the OpenWeather API using
Azure Data Factory and processes it using Azure Databricks.

Pipeline steps:
1. Extract weather data from API
2. Store raw JSON in Azure Data Lake (Bronze layer)
3. Flatten nested JSON using PySpark
4. Store clean dataset in Delta format
