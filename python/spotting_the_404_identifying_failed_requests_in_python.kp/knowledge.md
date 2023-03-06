---
title: How can you determine if you're receiving a 404 error when making a request?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can check if you`re getting a 404 in Python by checking the status code of the response object using `.status\_code`.
---

**Contents**

[TOC]

# Introduction
A 404 error code indicates that the requested resource is not found on the server. In Python, you may encounter 404 errors when making requests to external APIs or web pages. In this article, we will discuss how to identify a 404 error in Python.

# Sending a Request in Python
To make a request in Python, you can use the `requests` module. This module provides a simple way to send HTTP/1.1 requests. Here's an example of sending a request to a URL using Python:

```python
import requests

url = "https://www.example.com"
response = requests.get(url)

print(response.status_code)
```

The `get` method is used to send a GET request to the specified URL. The `response` object contains the server's response to the request, including the status code.

# Identifying a 404 Error
To identify a 404 error in Python, you can check the status code of the server's response. A 404 status code indicates that the requested resource was not found on the server.

```python
import requests

url = "https://www.example.com/invalid"

response = requests.get(url)

if response.status_code == 404:
    print("Resource not found!")
```

In the above example, we added `/invalid` to the URL, which does not exist on the server. The server will return a 404 status code to indicate that the requested resource is not available.

# Handling a 404 Error
When you encounter a 404 error in Python, you can handle it in different ways. One way is to raise an exception to notify the user that the requested resource was not found.

```python
import requests

url = "https://www.example.com/invalid"

response = requests.get(url)

if response.status_code == 404:
    raise Exception("Resource not found!")
```

In this case, we used the `raise` keyword to raise an exception with a custom error message. This will stop the program execution and print the error message to the user.

# Conclusion
In this article, we have discussed how to identify a 404 error in Python. We used the `requests` module to send a request to a URL and check the server's response status code. We also demonstrated how to handle a 404 error by raising an exception.
