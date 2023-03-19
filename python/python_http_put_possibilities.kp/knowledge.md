---
title: Can http put be executed using Python in any manner?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, the requests library in Python supports HTTP PUT requests.
---

**Contents**

[TOC]

Yes, there are several ways to do HTTP PUT in Python.

### Using requests library

The requests library is one of the most popular Python libraries used for making HTTP requests. To make a PUT request using the requests library, you can use the requests.put() method. Here's an example:

```python
import requests

url = 'http://example.com/api/user/1'
data = {'name': 'John Doe', 'age': 30}

response = requests.put(url, json=data)

print(response.status_code)
```

In this example, we're sending a PUT request to update a user's information. We're providing the user's ID in the URL and the data to be updated in the request body as a JSON object.

### Using urllib library

The urllib library in Python provides several modules for working with URLs. To make a PUT request using urllib, you can use the urllib.request.urlopen() method. Here's an example:

```python
import urllib.request
import json

url = 'http://example.com/api/user/1'
data = {'name': 'John Doe', 'age': 30}

req = urllib.request.Request(url, method='PUT')
req.add_header('Content-Type', 'application/json')
req.data = json.dumps(data).encode('utf-8')

response = urllib.request.urlopen(req)

print(response.status)
```

In this example, we're sending a PUT request to update a user's information. We're providing the user's ID in the URL and the data to be updated in the request body as a JSON object.

### Using httplib2 library

The httplib2 library is another popular Python library used for making HTTP requests. To make a PUT request using httplib2, you can use the httplib2.Http.request() method. Here's an example:

```python
import httplib2
import json

url = 'http://example.com/api/user/1'
data = {'name': 'John Doe', 'age': 30}

http = httplib2.Http()

response, content = http.request(url, method='PUT', body=json.dumps(data), headers={'Content-Type': 'application/json'})

print(response.status)
```

In this example, we're sending a PUT request to update a user's information. We're providing the user's ID in the URL and the data to be updated in the request body as a JSON object.

### Using restkit library

The restkit library is a lightweight and flexible HTTP client library for Python. To make a PUT request using restkit, you can use the restkit.request() method. Here's an example:

```python
import restkit
import json

url = 'http://example.com/api/user/1'
data = {'name': 'John Doe', 'age': 30}

response = restkit.request(url, method='PUT', payload=json.dumps(data), headers={'Content-Type': 'application/json'})

print(response.status)
```

In this example, we're sending a PUT request to update a user's information. We're providing the user's ID in the URL and the data to be updated in the request body as a JSON object.
