---
title: How to directly export a dataframe to csv format and save it to s3 in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `to\_csv` method with the s3 file path and AWS credentials configured to write the dataframe directly to an S3 bucket in csv format.
---

**Contents**

[TOC]

Section 1: Introduction

In this tutorial, we will learn how to save a Pandas DataFrame to a CSV file directly to an Amazon S3 bucket using Python. Amazon S3 is a cloud storage solution that enables you to store and retrieve data from anywhere on the web. It is scalable, reliable, and provides flexible data access controls. By the end of this tutorial, you will be able to programmatically export any data frame to .csv format directly to your Amazon S3 bucket.

We will be using the following Python libraries:

- Boto3: AWS SDK for Python, which enables Python developers to write software that interacts with services like Amazon S3 and Amazon EC2.
- Pandas: provides easy-to-use data structures and data analysis tools for the Python programming language.

Section 2: Setting Up S3 Bucket and Credentials

Before we proceed with uploading CSV directly to S3, we need to set up the S3 bucket, create access keys and configure the credentials. Here are the steps for setting up S3 bucket and credentials:

1. Create an AWS Account: If you don't have an AWS account, create one.

2. Create an S3 bucket: Once you have created the account, create an S3 bucket where you want to upload the CSV file. Make sure you remember the AWS region in which the bucket was created.

3. Create an Access Key and Secret Key: Navigate to the IAM console, and click on the user for which you want to create the Access key and Secret key. Create a new Access key and Secret key for the user. Make sure you save the keys as it will be required in the Python code.

4. Configure the credentials: Open your command prompt or terminal, type "aws configure" and follow the given instructions. Enter the Access Key ID and Secret Access Key when prompted.

Section 3: Code for Uploading CSV to S3

Now we're ready to write a Python code that uploads a CSV file to the S3 bucket. Here’s the code for uploading a CSV file to the S3 bucket, using the pandas and boto3 libraries.

``` python
import pandas as pd
import boto3

# create dataframe
df = pd.DataFrame({'Name': ['John', 'Smith', 'Paul', 'Lea'], 'Age': [26, 31, 23, 40]})

# set AWS credentials
aws_access_key_id = 'your_aws_access_key_id'
aws_secret_access_key = 'your_aws_secret_access_key'

# set S3 region and bucket
region = 'your_aws_s3_region'
bucket_name = 'your_aws_bucket_name'

# convert dataframe to csv and save it to s3
csv_buffer = df.to_csv(index=False).encode()
s3_resource = boto3.resource('s3', aws_access_key_id=aws_access_key_id, aws_secret_access_key=aws_secret_access_key, region_name=region)
s3_resource.Object(bucket_name, 'data.csv').put(Body=csv_buffer)
```

This Python code creates a sample Pandas DataFrame and saves it as a CSV file to an S3 bucket defined by the `bucket_name` variable. The `to_csv` method converts the data frame to a CSV file, which is then converted to a bytes object by using the `encode()` method. Finally, the `put()` method is used to upload the CSV file to the S3 bucket.

Section 4: Conclusion

In this tutorial, we have learned how to save a Pandas DataFrame to a CSV file directly to an Amazon S3 bucket using Python. First, we set up the S3 bucket and credentials. Then, we used the Pandas and Boto3 libraries to create and upload the CSV file to the S3 bucket. If you have any questions or comments, feel free to leave them in the comment section below.
