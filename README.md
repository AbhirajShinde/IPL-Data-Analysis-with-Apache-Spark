# Project Title
IPL Data Analysis with Apache Spark

# Project Description
This project demonstrates an end-to-end data processing and visualization pipeline using Databricks, Apache Spark, AWS, and SQL. The data, sourced from [data.world.com](https://data.world/), consists of detailed cricket match statistics which are stored and accessed from an AWS S3 bucket. The project involves defining custom schemas with Apache Spark, executing SQL queries, and generating insightful visualizations with Matplotlib and seaborn to analyze the performances across different matches.

# Technologies Used
- Databricks: Used for running Spark jobs and managing the cluster.
- Apache Spark: Utilized for data processing and executing SQL queries.
- AWS S3: Used for data storage and making data publicly accessible.
- SQL: Applied for data querying within Spark.
- Matplotlib and seaborn: Used for creating data visualizations.
- Data.world: Source of the dataset used in the analysis.

# Setting Up AWS Account and S3 Bucket:
1. Create an AWS Account:
- Go to the AWS homepage (https://aws.amazon.com/) and click on "Create an AWS Account."
- Follow the instructions to create your AWS account. You will need to provide payment information, but you can use the free tier for many services.
2. Access AWS Management Console:
- Once your account is set up, log in to the AWS Management Console.
3. Create an S3 Bucket:
- In the AWS Management Console, navigate to the S3 service.
- Click on "Create bucket" to create a new bucket.
- Choose a unique name for your bucket and select a region.
- Leave the settings as default or customize as needed.
- Click "Create bucket" to create the S3 bucket.
4. Make Objects Publicly Accessible:
- Select the bucket you created from the S3 dashboard.
- Navigate to the "Permissions" tab.
- Click on "Bucket Policy" and add a policy to make objects publicly accessible. Here's a sample policy:
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}
```
- Replace "your-bucket-name" with the name of your bucket.
- Click "Save" to apply the policy.

# Signing Up for Databricks Community Edition and Creating a Notebook:
1. Sign Up for Databricks:
- Go to the Databricks website (https://databricks.com/try-databricks) and sign up for the Community Edition.
- Follow the instructions to create your Databricks account.
2. Access Databricks Workspace:
- Once your account is created, log in to the Databricks workspace.
3. Create a Cluster:
- In the Databricks workspace, navigate to the Clusters tab.
- Click on "Create Cluster" to create a new cluster.
- Configure the cluster settings as needed and click "Create Cluster" to create the cluster.
4. Create a Notebook:
- In the Databricks workspace, navigate to the Workspace tab.
- Click on "Create" and select "Notebook" from the dropdown menu.
- Give your notebook a name and select the language as "Python."
- Click "Create" to create the notebook.