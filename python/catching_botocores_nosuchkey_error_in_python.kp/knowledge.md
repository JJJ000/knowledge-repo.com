---
title: What is the method of catching the nosuchkey exception in botocore?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: You can capture botocore`s NoSuchKey exception by using a try-except block and specifying botocore.exceptions.NoSuchKey as the exception to catch.
---

**Contents**

[TOC]

# Introduction
Botocore is a low-level interface to interact with AWS services in Python. In some cases, we may encounter exceptions while trying to perform operations with these services. In this tutorial, we will learn how to capture the NoSuchKey exception that may occur while working with the S3 service in AWS.

## The exception
The NoSuchKey exception is raised when an object in the S3 bucket is not found. This exception is a part of the botocore.exceptions module. 

## Handling the exception
To handle this exception, we need to use try-except blocks in our code. The following sections will explain how we can do this.

# Try-except block
Using the try-except block is the easiest way to capture the NoSuchKey exception raised by botocore. 

```python
import botocore

try:
    # Code to interact with S3
except botocore.exceptions.NoSuchKey:
    # Handle the exception
```
In the above code, if the `NoSuchKey` exception is raised, the code inside the `except` block will execute.

# Catching the exception message
We can also capture the exception message using the following code:

```python
import botocore

try:
    # Code to interact with S3
except botocore.exceptions.NoSuchKey as e:
    print(f'Exception message: {e}')
```
In the above code, the `e` object will contain the exception message, which we can then print to the console.

# Example code
Here is an example code snippet that uses the try-except block to capture the `NoSuchKey` exception:

```python
import boto3
import botocore

s3 = boto3.client('s3')

try:
    s3.head_object(Bucket='my-bucket', Key='non-existing-key')
except botocore.exceptions.NoSuchKey as e:
    print(f'Exception message: {e}')
```
In this example, we are trying to retrieve metadata about an object in the S3 bucket using the `head_object()` method. However, we are passing a non-existing key. Hence, the `NoSuchKey` exception is raised, which we then capture using the `except` block and print the exception message to the console.

# Conclusion
In this tutorial, we learned how to capture the `NoSuchKey` exception raised by botocore while interacting with the S3 service in AWS. We also learned how to handle the exception, capture the exception message, and saw an example of how to use the try-except block to catch the exception.
