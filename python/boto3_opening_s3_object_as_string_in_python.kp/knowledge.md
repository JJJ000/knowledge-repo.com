---
title: Use boto3 to access an s3 object and convert it into a string format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `get\_object()` method from the `boto3.resource(`s3`)` object to retrieve the contents of a file in S3 as a string.
---

**Contents**

[TOC]

## Importing Necessary Modules

To open an S3 object as a string with Boto3 in Python, we need to import some necessary modules. 

```python
import boto3
from botocore.exceptions import NoCredentialsError
```

## Creating an S3 Client

The next section would be creating an S3 client. We can achieve that by specifying AWS access key, secret key, and the S3 region as shown below.

```python
Access_key = 'your_access_key'
Secret_key = 'your_secret_key'
Region = 'your_aws_region'

s3 = boto3.client('s3',
                  aws_access_key_id = Access_key,
                  aws_secret_access_key = Secret_key,
                  region_name = Region)
```

## Opening S3 Object as a String

Once we have created the S3 client, we can open an S3 object as a string by using the `get_object` method of the S3 client and then converting the returned object to a string using the `Body` attribute.

```python
bucket_name = 'your_bucket_name'
file_name = 'your_file_name'

try:
    s3_response_object = s3.get_object(Bucket=bucket_name, Key=file_name)
    object_content = s3_response_object['Body'].read().decode('utf-8')
    print(object_content)
except NoCredentialsError:
    print("Credentials not available")
```

The `get_object` method takes two parameters - the bucket name and the file name that you want to open as a string. 

The `Body` attribute of the returned object contains the contents of the file, which we read using the `read` method and then convert to a string using the `decode` method with the `utf-8` encoding. 

Finally, we print the contents of the file as a string. If there are no credentials, we print a message indicating that the credentials are not available.

These are the necessary steps involved in opening an S3 object as a string with Boto3 in Python.
