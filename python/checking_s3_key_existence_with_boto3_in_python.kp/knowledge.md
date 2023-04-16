---
title: Determine if a key exists in an s3 bucket using boto3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a key exists in a bucket in s3 using boto3 in Python by calling the s3.Bucket.Object.exists() method.
---

**Contents**

[TOC]

### Initialize the S3 Client

The first step is to initialize the S3 client. This can be done by using the `boto3` library.

```python
import boto3

s3 = boto3.client('s3')
```

### Check if a Key Exists

Once the S3 client is initialized, the `head_object()` method can be used to check if a key exists in the specified bucket.

```python
response = s3.head_object(Bucket='my-bucket', Key='my-key')
```

### Check Response

The response will be a dictionary containing information about the object, such as its size, content type, and last modified date. If the key does not exist, the response will be `None`.

```python
if response is not None:
  print('Key exists')
else:
  print('Key does not exist')
```

### Handle Errors

It is important to handle any errors that may occur when checking if a key exists. An error will be raised if the bucket or key does not exist, or if the user does not have permission to access the bucket.

```python
try:
  response = s3.head_object(Bucket='my-bucket', Key='my-key')
except ClientError as e:
  # handle the exception
  print(e)
```
