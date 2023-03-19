---
title: What is the procedure for using boto3 to save an s3 object to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Call the `download\_file()` method of the S3 resource object and pass in the S3 bucket name and object key as well as the local file name to save the object.
---

**Contents**

[TOC]

## Installing boto3

Before we start using boto3, we need to install it. You can install boto3 using pip. Open your terminal or command prompt and run the command `!pip install boto3`.

## Creating an S3 client

To interact with S3 using boto3, we first need to create an S3 client. We can create an S3 client using the following Python code:

```python
import boto3

s3_client = boto3.client('s3')
```

The `boto3.client('s3')` line creates an S3 client, which can be used to upload, download or delete objects from your S3 bucket.


## Saving an S3 object to a file

Once we have our S3 client set up, we can download an S3 object to a file using the following Python code:

```python
import boto3

s3_client = boto3.client('s3')

s3_bucket_name = 'my-bucket-name'
s3_object_key = 'my-object-key'
local_file_path = '/path/to/local_file'

with open(local_file_path, 'wb') as f:
    s3_client.download_fileobj(s3_bucket_name, s3_object_key, f)
```

In the above code, we provide the S3 bucket name, object key and local file path that we want to save the S3 object to. We then open a file in `write binary` mode, and use the `s3_client.download_fileobj` function to download the S3 object to the file.

Once the `with` block is complete, the file will be saved to `local_file_path`.

## Putting it all together

Here is the code that combines everything together:

```python
import boto3

s3_client = boto3.client('s3')

s3_bucket_name = 'my-bucket-name'
s3_object_key = 'my-object-key'
local_file_path = '/path/to/local_file'

with open(local_file_path, 'wb') as f:
    s3_client.download_fileobj(s3_bucket_name, s3_object_key, f)

print(f'Successfully saved S3 object {s3_object_key} to {local_file_path}')
```

In the example above, we print a message to the console once the file has been successfully saved.
