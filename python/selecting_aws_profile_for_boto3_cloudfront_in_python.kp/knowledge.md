---
title: What factors to consider while selecting an aws profile for establishing connectivity to cloudfront using boto3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can specify the AWS profile using the `profile\_name` parameter in the boto3 session constructor.
---

**Contents**

[TOC]

# Introduction
When it comes to using `boto3` to connect to CloudFront in Python, one may need to choose an AWS profile to use. In this article, we will discuss how to choose an AWS profile when using `boto3` to connect to CloudFront in Python.

## Step 1: Configure AWS CLI
Before using `boto3`, you should have the AWS CLI set up in your environment. AWS CLI is a command-line tool that provides an interface to manage your AWS services. To configure AWS CLI, follow these steps:

1. Install AWS CLI in your local machine. For more information, you can refer to the AWS CLI installation guide.

2. Once installed, configure AWS CLI with your AWS credentials by running the following command:

   ```
   aws configure
   ```

3. Enter your AWS Access Key ID and Secret Access Key. You can also enter your preferred default region and output format.

4. After the configuration is complete, you can verify it by running the following command:

   ```
   aws configure list
   ```

   This command will display your AWS credentials, default region, and output format.

## Step 2: Set the AWS Profile in your Python code
Once your AWS CLI is configured, you can choose an AWS profile to use in your Python code. To set the AWS profile, you can use the following code in your Python script:

```python
import boto3

session = boto3.Session(profile_name='<your_profile_name>')

client = session.client('cloudfront')

# Now you can use the CloudFront client to make requests to your CloudFront distribution
```

In this code snippet, we first create a `Session` object by passing the name of the AWS profile we want to use. We then create a `client` object for the CloudFront service using the `Session` object. Now you can use the CloudFront client to make requests to your CloudFront distribution.


## Conclusion
Choosing an AWS profile when using `boto3` to connect to CloudFront in Python is a simple process. First, you need to configure AWS CLI with your AWS credentials. Once that is done, you can set the AWS profile in your Python code using the `Session` object.
