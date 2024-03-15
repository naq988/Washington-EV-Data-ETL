# Washington-EV-Data-ETL

Project objective: To create an ETL (Extract-Transform-Load) pipeline that extracts a public dataset from Washington State's Department of Licensing containing Electric Vehicle registration data, transforms/cleans the data, and then loads the data into an AWS S3 bucket. The data will then be moved into one of AWS's RDS services, such as Aurora or Athena, so that data analysis can be performed using SQL and important insights can be drawn from the data. Finally, AWS Quicksight will be used to create a dashboard containing important metrics/data visualizations.

Project plan
1. Create a python script that uses the following libraries: requests, polars, and boto3. First, the requests library will be used to download the dataset csv from data.gov and store it into a path on local machine.
2. Then, Polars will be used to perform data cleaning to handle missing values, drop unnecessary columns, etc.
3. Once the data is cleaned, we use the Boto3 library to write the csv to an S3 bucket.
4. Make it so that the data is immediately pushed to the database upon being written to the S3 bucket using AWS Lambda script also written in Python.
5. Using RDS, we create a database and load it with the csv from the S3 bucket.
6. Once the data is loaded into the database, we can use SQL to analyze data and draw insights.
7. Lastly, we connect our csv to AWS Quicksight so that we can create a dashboard containing visualizations. The goal is to make the data update once new rows of data are added to the database.

Error handling: Make it so that the pipeline doesn't break no matter the scenario. For example, if the website the source data is from is temporarily down the time the pipeline is scheduled to run, it should be able to handle this. If the columns in the csv from the source change, the pipeline should be able to handle this.

Things to consider later:
Data validation - look into Great Expectations library
Using Lambda for error handling using try-catch blocks, retry behavior, 
Pagination for breaking the data into smaller more managable chunks
Automated testing

Some insights I hope to explore with this project are:
1. EV Adoption Trends Over Time: Analyze the growth rate of the total number of EVs registered with DOL over time
2. Popular Makes and Models: Identify which makes and models of electric vehicles are most popular
3. Geographical Distribution of EVs: Analyze which cities/counties in Washington State have higher concentrations of registered EVs
4. Type of Electric Vehicles: Analyze and identify the distribution between Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles.
5. Vehicle Ranges: Investigate how the range of EVs varies among different makes and models. In addition, identify any trends over the years to see which make/model has improved its range the most.
6. Machine Learning Insights: Utilize ML features to provide forecasting and anomaly detection

Technologies used:
Programming: Python | DB: PostgresSQL | AWS: S3 for storage, Lambda for serverless event-driven computing, Redshift/Aurora/Athena for Relational Database, Quicksight for BI capabilities | Version Control: Git | Infrastructure as Code (IAC): Terraform 

Skills used:
API requests, data extraction, data cleaning, data validation, ETL development, exception handling, data analytics, data visualization

The goal is to include a jupyter notebook, as well as a flowchart diagram showing the whole process step-by-step.
