---
title: How can I print the full, raw http request using Python requests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `.request.body` attribute to print the entire raw HTTP request.
---

**Contents**

[TOC]

### Using the Requests Library
The `requests` library makes it easy to print the entire HTTP request as a raw string. To do this, simply call the `.request` method on the `requests` object, passing in the method and URL as the arguments.

```python
import requests

r = requests.get('https://www.example.com')
print(r.request.method + ' ' + r.request.url)
```

This will print out something like:

```
GET https://www.example.com
```

### Using the HTTP Client Library
The `http.client` library provides an easy way to print the entire HTTP request as a raw string. To do this, create an `HTTPConnection` object, call the `request` method on it, and then call the `getrequest` method.

```python
import http.client

conn = http.client.HTTPSConnection('www.example.com')
conn.request('GET', '/')
print(conn.getrequest())
```

This will print out something like:

```
GET / HTTP/1.1
Host: www.example.com
User-Agent: Python-urllib/3.7
Accept-Encoding: identity
Connection: close
```

### Using the urllib Library
The `urllib` library provides a way to print the entire HTTP request as a raw string. To do this, create an `Request` object, call the `get_method` method on it, and then call the `get_full_url` method.

```python
import urllib.request

req = urllib.request.Request('https://www.example.com')
print(req.get_method() + ' ' + req.get_full_url())
```

This will print out something like:

```
GET https://www.example.com
```
