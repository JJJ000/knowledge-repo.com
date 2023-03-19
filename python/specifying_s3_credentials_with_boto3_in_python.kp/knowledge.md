---
title: What is the procedure for specifying credentials when establishing a connection to boto3 s3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can specify the access key and secret key as arguments when creating an S3 client using the boto3 library in Python.
---

**Contents**

[TOC]

## Introduction
Boto3 is a software development kit (SDK) for the Amazon Web Services (AWS) that allows users to access and manage AWS resources through their Python code. Boto3 provides a simple, easy-to-use interface that allows for integration with AWS services such as S3. In this article, we will discuss how to specify credentials when connecting to Boto3 S3 in Python.

## Creating AWS credentials
To specify credentials when connecting to Boto3 S3 in Python, you first need to create an AWS account if you don't already have one. Once you have an AWS account, you can create an Access Key ID and Secret Access Key, which will be used to authenticate your Python code when connecting to AWS resources. Here are the steps to create AWS credentials:

1. Login to your AWS account.
2. Click on your username in the top-right corner of the screen, and select "My Security Credentials" from the dropdown menu.
3. In the "Access keys (access key ID and secret access key)" section, click on "Create New Access Key".
4. Save your Access Key ID and Secret Access Key in a safe place, as they will not be shown again.

## Specifying credentials in Python
After creating AWS credentials, you can specify them in your Python code to authenticate your connection to AWS resources. Boto3 allows you to specify credentials in several ways, which are as follows:

### Method 1: Hardcoding credentials
You can hardcode your credentials directly into your Python code using the `boto3.Session` object. Here's an example:

```python
import boto3

session = boto3.Session(
    aws_access_key_id='ACCESS_KEY_ID',
    aws_secret_access_key='SECRET_ACCESS_KEY',
)
s3 = session.resource('s3')
```

### Method 2: Environment variables
You can also set your credentials as environment variables in your operating system. Here's an example:

```python
import boto3
import os

os.environ['AWS_ACCESS_KEY_ID'] = 'ACCESS_KEY_ID'
os.environ['AWS_SECRET_ACCESS_KEY'] = 'SECRET_ACCESS_KEY'

s3 = boto3.resource('s3')
```

### Method 3: Credential file
You can store your credentials in a credential file on your local system, and Boto3 will automatically load them. Here are the steps to create a credential file:

1. Create a new file named `~/.aws/credentials` and enter the following:

```conf
[default]
aws_access_key_id = ACCESS_KEY_ID
aws_secret_access_key = SECRET_ACCESS_KEY
```

2. In your Python code, you can connect to S3 using the following:

```python
import boto3

s3 = boto3.resource('s3')
```

Boto3 will automatically use the credentials from the `~/.aws/credentials` file.

## Conclusion
In this article, we discussed how to specify credentials when connecting to Boto3 S3 in Python. We covered three ways of specifying the credentials: hardcoded credentials, environment variables, and credential files. By following these steps, you should now be able to connect to S3 using Boto3 with ease.
