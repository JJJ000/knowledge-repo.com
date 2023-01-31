---
title: How can I perform an http get request quickly in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The quickest way to HTTP GET in Python is to use the requests library.
---

**Contents**

[TOC]

# Using the Requests Library
The [requests](http://docs.python-requests.org/en/master/) library is the quickest way to send an HTTP GET request in Python. Requests is an elegant and simple HTTP library for Python, built for human beings. It abstracts the complexities of making requests behind a beautiful, simple API so that you can focus on interacting with services and consuming data in your application.

# Installation
To install requests, simply use pip:

```
pip install requests
```

# Usage
To make a GET request with requests, you can use the get method:

```
import requests

url = 'http://example.com'

response = requests.get(url)

print(response.text)
```

# Response
The response object contains all the information returned by the server, such as the status code, headers, and the response body. You can access the response body using the text attribute:

```
print(response.text)
```
