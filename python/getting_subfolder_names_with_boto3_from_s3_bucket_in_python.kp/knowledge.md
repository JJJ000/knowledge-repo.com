---
title: Getting the names of subfolders in an s3 bucket using boto3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use boto3 list\_objects\_v2 method with Prefix set to the subfolder path to retrieve subfolder names in S3 bucket.
---

**Contents**

[TOC]

## Introduction
Amazon Simple Storage Service (S3) is a highly scalable and durable object storage service. It allows developers to store and retrieve any amount of data from anywhere on the web. S3 stores data as objects within buckets. In this tutorial, we will learn how to retrieve the names of all the subfolders in an S3 bucket using boto3 in Python.

## Prerequisites
To follow this tutorial, you will need:

* An AWS account
* Python 3.x installed on your computer
* Boto3 library installed in your virtual environment


## Retrieving subfolder names in S3 bucket
To retrieve the names of all the subfolders in an S3 bucket, we can use boto3 library in Python. Boto3 provides simple interface for interacting with the S3 service. Here is the code to retrieve the subfolder names in S3 bucket:

```python
import boto3


def get_subfolder_names(bucket_name):
    """
    Get the names of all the subfolders in a bucket.
    """
    s3 = boto3.client('s3')
    response = s3.list_objects_v2(Bucket=bucket_name, Delimiter='/')
    for content in response.get('CommonPrefixes'):
        yield content.get('Prefix')
```

## Explanation
The `get_subfolder_names` function takes the name of the S3 bucket as its only argument. The function first creates an S3 client object using the `boto3.client` method. 

Next, it calls `s3.list_objects_v2` method with a Delimiter parameter set to `/`. This ensures that only the subfolders are returned and not the objects present in the bucket. 

The `list_objects_v2` method returns a dictionary containing the metadata for the objects and the subfolders in the bucket. We iterate over the `CommonPrefixes` key of the dictionary and extract the `Prefix` key from each dictionary item. 

The `Prefix` key holds the name of the subfolder. We yield the value of the `Prefix` key to the caller using a generator.

## Conclusion
In this tutorial, we learned how to retrieve the names of all the subfolders in an S3 bucket using boto3 in Python. We used the `list_objects_v2` method and set the Delimiter parameter to `/` to ensure that only the subfolders are returned. We then iterated over the `CommonPrefixes` key of the response dictionary and extracted the `Prefix` key from each item. Finally, we yielded the subfolder name to the caller using a generator.
