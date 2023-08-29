# Parallel processing ETL pipeline using Apache Airflow and AWS

This pipeline fetches live weather data for Houston, Texas, transforms it into a structured format, and combines it with essential city lookup information. The result is enriched data that is saved in both a PostgreSQL database and an S3 bucket. The project leverages AWS services including RDS (Relational Database Service), EC2 (Elastic Compute Cloud), S3 (Simple Storage Service: Ubuntu), and IAM (Identity and Access Management) for secure and efficient data management. This data pipeline harnesses the parallel processing capabilities of Airflow, running tasks simultaneously for optimized performance.

## Pipeline Workflow
- *Task Initialization:* The pipeline starts with a task to initiate the workflow.
- *Parallel Processing:* Utilizing Airflow's Task Groups, the pipeline extracts, transforms, and loads data simultaneously from different sources.
- *Data Extraction:* The OpenWeather API provides real-time weather data for Houston.
- *Data Transformation:* Temperature values are converted from Kelvin to Fahrenheit, enhancing data accuracy.
- *City Lookup:* Essential city lookup information is combined with the weather data using PostgreSQL's join operation.
- *Data Loading:* Transformed and joined data is loaded into PostgreSQL and saved as enriched CSV files in an S3 bucket.
- *Task Completion:* The pipeline concludes with tasks indicating successful execution.

<img width="1147" alt="Screenshot 2023-08-29 at 12 01 19 AM" src="https://github.com/alyona-vishnoi/parallel-processing-ETL-pipeline/assets/88257366/98e19d58-a9fa-4fc3-8001-e59b66c00d55">

Weather API: https://openweathermap.org/api 
