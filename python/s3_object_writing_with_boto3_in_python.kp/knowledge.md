---
title: What is the process for using boto3 to save a file or data as an s3 object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To write a file or data to an S3 object using boto3 in Python, use the `put\_object()` method with the appropriate parameters.
---

**Contents**

[TOC]

## Introduction

Amazon S3 is a cloud-based storage platform that provides scalable and secure data storage and retrieval capabilities. Boto3 is a Python-based SDK that provides an interface to Amazon Web Services (AWS) services. In this article, we will take a look at how we can use boto3 to write files or data to an S3 bucket.

## Prerequisites

Before we get started, we need to ensure that we have the following:

1. An AWS account
2. Access key and secret access keys
3. Access to an S3 bucket
4. Python 3.x
5. The boto3 Python library.

## Installing Boto3

We can install boto3 using pip, as shown below:

```
pip install boto3
```

## Writing to an S3 object using Boto3

To write a file or data to an S3 object using boto3, we need to perform the following steps:

1. Import the necessary libraries
2. Create an S3 client
3. Write the file or data to an S3 object

### Importing the Required Libraries

We begin by importing the necessary libraries as shown below:

```
import boto3
```

### Creating an S3 Client

Next, we need to create an S3 client using the `boto3.client()` function. We also need to provide our AWS access key and secret access key, which we can do by passing them as arguments to the `client()` function:

```
s3 = boto3.client('s3', aws_access_key_id=<access-key>,
    aws_secret_access_key=<secret-access-key>)
```

### Writing the File or Data to an S3 Object

Finally, we can write the file or data to an S3 object using the `put_object()` function:

```
response = s3.put_object(Bucket=<bucket-name>, Key=<object-key>, Body=<file-or-data>)
```

Let's take a closer look at each parameter:

- `Bucket`: The name of the S3 bucket where we want to write the file or data.
- `Key`: The key or path to the S3 object we want to create.
- `Body`: The contents of the file or data we want to write.

Here is an example that writes a file to an S3 object:

```
import boto3

s3 = boto3.client('s3', aws_access_key_id=<access-key>,
    aws_secret_access_key=<secret-access-key>)

with open(<local-file-path>, 'rb') as f:
    s3.upload_fileobj(f, <bucket-name>, <object-key>)
```

This code reads the file at `<local-file-path>` and uploads it to the S3 object with key `<object-key>` in the `<bucket-name>` bucket. If the file is large or if we want to send the file in chunks, we can use the `upload_file()` or `upload_fileobj()` functions provided by the S3 client to optimize the transfer.

## Conclusion

In this article, we looked at how we can use boto3 to write files or data to an S3 bucket. We began by installing the necessary libraries and then created an S3 client. Finally, we wrote the file or data to an S3 object using the `put_object()` function. By following these steps, we can easily write files or data to an S3 bucket in our Python applications.
