---
title: Viewing the items in an amazon s3 bucket using boto3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The contents of a bucket can be listed using the boto3 Bucket.objects.all() method.
---

**Contents**

[TOC]

# Listing Bucket Contents

## Prerequisites

Before attempting to list the contents of a bucket, you will need the following:

- A valid AWS account 
- Access to the AWS Console
- An S3 bucket with objects
- The boto3 library installed

## Connect to S3

The first step is to connect to the S3 service using boto3. This can be done using the following code:

```python
import boto3

# Create an S3 client
s3 = boto3.client('s3')
```

## List the Contents of a Bucket

Once connected to S3, you can list the contents of a bucket by using the `list_objects_v2()` method. This method takes in the `Bucket` parameter, which is the name of the bucket to list the contents of. The following code will list the contents of an S3 bucket:

```python
# List the contents of a bucket
response = s3.list_objects_v2(
    Bucket='my-bucket-name'
)

# Print the contents of the bucket
for content in response['Contents']:
    print(content['Key'])
```

## Output

The output of this code will be a list of the objects in the bucket, each on its own line. For example:

```
object1.txt
object2.txt
object3.txt
```
