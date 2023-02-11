---
title: Retrieving a JSON file from an s3 bucket using Python boto3
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can read a JSON file from S3 using Python boto3 by calling the boto3.client(`s3`).get\_object() method.
---

**Contents**

[TOC]

#### Section 1: Setup

Before we can read the JSON file from S3, we need to set up the necessary environment for boto3. To do this, we must first install boto3 and configure our AWS credentials. 

#### Section 2: Import Libraries

Once we have our environment set up, we can then import the boto3 library and other necessary libraries.

```python
import boto3
import json
```

#### Section 3: Connect to S3

Next, we will create a connection to S3 using the boto3 library. We will need to provide the Access Key ID and Secret Access Key for our AWS account.

```python
s3 = boto3.client('s3',
    aws_access_key_id=ACCESS_KEY_ID,
    aws_secret_access_key=SECRET_ACCESS_KEY
)
```

#### Section 4: Read JSON File

Finally, we can read the JSON file from S3 using the boto3 library. We will need to provide the bucket name and file name for the JSON file.

```python
obj = s3.get_object(Bucket=BUCKET_NAME, Key=FILE_NAME)
data = json.loads(obj['Body'].read())
```

Once we have the data, we can access it and use it as needed.
