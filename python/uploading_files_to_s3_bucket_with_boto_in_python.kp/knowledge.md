---
title: What is the process for uploading a file to a directory in an s3 bucket using boto?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `upload\_file` method of the `S3` object in the Boto3 library to upload a file to a specific directory in an S3 bucket.
---

**Contents**

[TOC]

## Connecting to Boto and S3 bucket

The first step in uploading a file to an S3 bucket using Boto is to establish a connection with the S3 bucket using Boto. To do this, we need to provide AWS account details, including access and secret keys, region, and bucket name. We can use the `connect_s3()` method of the `boto.s3.connection` module to establish a connection with the S3 bucket.

```python
import boto
import boto.s3.connection

# AWS account details
access_key = '<access_key_here>'
secret_key = '<secret_key_here>'
region = '<aws_region_here>'
bucket_name = '<bucket_name_here>'

# Establish a connection with S3 bucket
conn = boto.connect_s3(
    aws_access_key_id=access_key,
    aws_secret_access_key=secret_key,
    region_name=region,
)

bucket = conn.get_bucket(bucket_name)
```

## Uploading File using Key

The next step is to upload the file to the S3 bucket using the `Key` object. We create a `Key` object using the `Bucket.new_key()` method and specify the filename as the key name. We then use the `Key.set_contents_from_filename()` method to upload the file to the S3 bucket.

```python
import os

# File to upload
file_path = '<file_path_here>'
file_name = '<file_name_here>'
key_name = os.path.join('<path_in_bucket>', file_name)

# Create Key object
k = bucket.new_key(key_name)

# Upload file to S3 bucket
k.set_contents_from_filename(file_path)
```

## Uploading File using File Object

Alternatively, we can also upload files to the S3 bucket using a file object. We can use the `Key.set_contents_from_file()` method to upload the file to the S3 bucket using a file object.

```python
import os

# File to upload
file_path = '<file_path_here>'
file_name = '<file_name_here>'
key_name = os.path.join('<path_in_bucket>', file_name)

# Create Key object
k = bucket.new_key(key_name)

# Upload file to S3 bucket using file object
with open(file_path, 'rb') as f:
    k.set_contents_from_file(f)
```

## Uploading Large Files using Multipart Upload

If we need to upload large files to the S3 bucket, we can use the multipart upload feature of S3 to upload the files in parts. We can use the `initiate_multipart_upload()` method to start a multipart upload and the `upload_part_from_file()` method to upload parts of the file. Finally, we can use the `complete_multipart_upload()` method to complete the upload.

```python
import os

# Large File to upload
large_file_path = '<large_file_path_here>'
large_file_name = '<large_file_name_here>'
key_name = os.path.join('<path_in_bucket>', large_file_name)

# Create Key object
k = bucket.new_key(key_name)

# Start multipart upload
mp = k.initiate_multipart_upload()

# Upload parts of the file
chunk_size = 50 * 1024 * 1024  # 50MB
chunk_count = int(math.ceil(os.path.getsize(large_file_path) / float(chunk_size)))
for i in range(chunk_count):
    offset = chunk_size * i
    byte_count = min(chunk_size, os.path.getsize(large_file_path) - offset)
    with open(large_file_path, 'rb') as f:
        f.seek(offset)
        mp.upload_part_from_file(fp=f, part_num=i + 1, size=byte_count)

# Complete multipart upload
mp.complete_upload()
```

Note: In the example above, we are uploading the large file in 50MB parts. We can adjust the `chunk_size` variable to specify the size of each part.
