---
title: What is the process for sending a "multipart/form-data" request using Python and the requests library?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `files` parameter of the requests.post() method to send a `multipart/form-data` with requests in python.
---

**Contents**

[TOC]

## Section 1: Importing Packages

Before sending a "multipart/form-data" request, you must import the necessary packages. To do this, you can use the `import` statement.

```python
import requests
```

## Section 2: Creating the Request

Next, you must create the request. To do this, you can use the `requests.post()` method. This method requires two arguments: the URL of the request and the data to be sent.

```python
url = 'http://example.com'
data = {'key1': 'value1', 'key2': 'value2'}

response = requests.post(url, data=data)
```

## Section 3: Setting the Content Type

In order to send a "multipart/form-data" request, you must set the content type of the request. To do this, you can use the `headers` argument of the `requests.post()` method.

```python
headers = {'Content-Type': 'multipart/form-data'}

response = requests.post(url, data=data, headers=headers)
```

## Section 4: Sending the Request

Finally, you can send the request by calling the `.send()` method on the response object.

```python
response.send()
```
