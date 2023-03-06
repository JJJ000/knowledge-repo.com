---
title: What is the procedure for uploading a file using Python requests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can upload a file using Python requests by using the `files` parameter with the post method.
---

**Contents**

[TOC]

## Section 1: Installing requests module

Before we start uploading files with requests, we need to install the requests module. To install the requests module, you can use the following command if you are using pip:

```python
pip install requests
```

## Section 2: Uploading file with requests module

To upload a file using the requests module, you need to create a Python script and import requests module. You can then use the requests.post() method to send a POST request to the server, along with the file data.

Here is a sample Python script that demonstrates how to upload a file with the requests module:

```python
import requests

file = {'file': open('test.txt', 'rb')}
response = requests.post('http://httpbin.org/post', files=file)

print(response.status_code)
print(response.text)
```

In this script, we are sending a POST request to the URL 'http://httpbin.org/post'. We are also passing the file data using the 'files' parameter of the post() method. The 'files' parameter is a dictionary containing the name of the file (in this case 'file') and the binary data of the file (which we are reading from 'test.txt' using the 'open()' method).

## Section 3: Sending additional data with the file

You can also send additional data along with the file data by passing a dictionary containing form data using the 'data' parameter of the post() method.

Here is a sample Python script that demonstrates how to send additional data along with the file:

```python
import requests

file = {'file': open('test.txt', 'rb')}
data = {'name': 'John Doe'}
response = requests.post('http://httpbin.org/post', files=file, data=data)

print(response.status_code)
print(response.text)
```

In this script, we are sending a dictionary containing the form data using the 'data' parameter. The 'data' parameter is a dictionary containing key-value pairs of form data. In this case, we are sending a form field named 'name' with the value 'John Doe'.

## Section 4: Uploading multiple files

You can also upload multiple files using the requests module by passing a list of dictionaries containing file data.

Here is a sample Python script that demonstrates how to upload multiple files:

```python
import requests

files = [
    ('file_1', open('test_1.txt', 'rb')),
    ('file_2', open('test_2.txt', 'rb'))
]
response = requests.post('http://httpbin.org/post', files=files)

print(response.status_code)
print(response.text)
```

In this script, we are uploading two files named 'test_1.txt' and 'test_2.txt'. We are passing the file data as a list of tuples containing the field name (in this case 'file_1' and 'file_2') and the binary data of the file. The server will receive the files with the corresponding field names.
