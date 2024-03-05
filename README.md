# Washington-EV-Data-ETL

Project objective: To create an ETL (Extract-Transform-Load) pipeline that extracts a public dataset from Washington State's Department of Licensing containing Electric Vehicle registration data, transforms/cleans the data, and then loads the data into an AWS S3 bucket. The data will then be moved into one of AWS's RDS services, such as Aurora or Athena, so that we can perform data analysis using SQL and draw important insights from the data. Finally, we will be using AWS Quicksight to create a dashboard containing important metrics/data visualizations.




1. We will use Python to write a script that uses the following libraries: requests, polars, and boto3. First, we will be using the requests library to download the dataset csv from data.gov and store it into a local path on my machine.
2. Then, we will use Polars to perform data cleaning to handle missing values, drop unnecessary columns, etc.
3. Once the data is cleaned, we use the Boto3 library to write the csv to an S3 bucket.
4. Using RDS, we create a database and load it with the csv from the S3 bucket.
5. Once the data is loaded into the database, we can use SQL to analyze data and draw insights.
6. Lastly, we connect our csv to AWS Quicksight so that we can create a dashboard containing visualizations. The goal is to make the data update once new rows of data are added to the database.




Technologies used:
Python, SQL, AWS S3, RDS, Quicksight

Skills used:
API requests, data extraction, data cleaning, ETL development, data analytics, data visualization

