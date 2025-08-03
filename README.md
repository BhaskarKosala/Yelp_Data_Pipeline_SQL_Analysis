# Yelp_Data_Pipeline_SQL_Analysis


# 📊 End-to-End Yelp Data Analysis using SQL, Python, AWS S3 & Snowflake

This project focuses on building a scalable data pipeline and conducting structured analysis on Yelp's large-scale review and business datasets.


# Flow Diagram of End to End Data Pipeline:

![image alt](https://github.com/BhaskarKosala/Yelp_Data_Pipeline_SQL_Analysis/blob/1fe0bf03880ea3af2292022250adcb187f1c2465/flow%20chart%20of%20data%20pipe%20line.jpg)


# 🚀 Workflow Summary:

**1. Data Source:**

- Yelp Reviews: 5GB JSON (~7 million records)

- Yelp Businesses: 113MB JSON (~150K records)

- Link to downlaod the dataset: https://business.yelp.com/data/resources/open-dataset/

**2. Data Engineering (ETL):**

- Used Python (Jupyter Notebook) to split the large JSON review file into 26 smaller chunks.

- Uploaded all JSON files (review + business) into an AWS S3 bucket using boto3 and access keys.

- Loaded S3 data into Snowflake using external stage configuration.

**3. Data Transformation:**

- Converted semi-structured JSON data into tabular format using FLATTEN, LATERAL, and PARSE_JSON.

- Defined schema and built views to structure nested data (e.g., users, stars, categories).

**4. Sentiment Analysis (UDF):**

- Created a User-Defined Function (UDF) in Snowflake to perform basic sentiment analysis on review texts.

**5. Data Analysis (SQL):**

- Wrote 10+ analytical SQL queries to derive insights such as:

- Top-rated businesses by category

- Most active reviewers

- Average ratings by location

- Review sentiment trends


# ⚙️ Tech Stack:

Python · AWS S3 · Snowflake · SQL · JSON · UDF · Jupyter Notebook · Cloud Data Pipeline · Sentiment Analysis
