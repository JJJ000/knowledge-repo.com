---
title: What is the process for handling errors in boto3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use try-except blocks to catch and handle exceptions raised by boto3 operations.
---

**Contents**

[TOC]

## Introduction

Boto3 is a Python library which provides an interface to interact with various Amazon Web Services (AWS). It is an essential tool for AWS developers and administrators. 

However, while working with Boto3, it is essential to handle errors that may occur while working with different AWS services. In this guide, we will take a look at some of the ways to handle errors when using Boto3.

## Try and Except Block

One of the most common ways to handle errors with Boto3 is to use the `try` and `except` blocks. This block will allow you to catch and handle any exception that may occur within your code.

For example, let's assume you want to create an S3 bucket with Boto3. If there is any issue creating the bucket, you can use the `try` and `except` blocks to handle the error.

```
import boto3

s3 = boto3.resource('s3')

try:  
    s3.create_bucket(Bucket='example_bucket')
except Exception as e:
    print(e)
```

In the above code, we are trying to create an S3 bucket with the name `example_bucket`. If there is any error during the creation of the bucket, the code will print the error.

## Handling Specific Errors

Sometimes, you may want to handle a specific error that occurs while working with Boto3. In such cases, you can catch that specific error using the `except` block.

For example, if you want to catch and handle the error that occurs when a bucket already exists, you can use the `BucketAlreadyExists` exception.

```
import boto3
from botocore.exceptions import ClientError

s3 = boto3.resource('s3')

try:
    s3.create_bucket(Bucket='example_bucket')
except ClientError as e:
    if e.response['Error']['Code'] == 'BucketAlreadyExists':
        print("Bucket already exists")
    else:
        print(e)
```

In the above code, the `if` statement checks if the error code is `BucketAlreadyExists`, and if it is, it will print the message "Bucket already exists."

## Using the Waiter

Some AWS services may take some time to complete an action. For example, when creating an EC2 instance, it may take a few seconds to launch the instance fully. In these cases, you can use the `waiter` object provided by Boto3 to wait until the action is completed.

For example, let's assume that you want to wait until an EC2 instance has finished launching before proceeding with your code. You can use the `wait_until_running` function provided by the EC2 waiter to wait until the instance is running.

```
import boto3

ec2 = boto3.resource('ec2', region_name='us-west-2')

instance = ec2.create_instances(
    ImageId='ami-1234567890abcdef0',
    MinCount=1,
    MaxCount=1,
    InstanceType='t2.micro'
)[0]

instance.wait_until_running()

print(instance.id, "is now running")
```

In the above code, we create an EC2 instance and use the `wait_until_running` function to wait until the instance is running. Once the instance is running, the code prints the instance ID and the message "is now running."

## Conclusion

In conclusion, handling errors when working with Boto3 is essential to ensure that your AWS applications run smoothly. You can handle errors using `try` and `except` blocks, handling specific errors, or using the `waiter` object provided by Boto3. By using these techniques, you can build robust and reliable AWS applications.
