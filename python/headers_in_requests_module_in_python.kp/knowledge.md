---
title: Rewording the process of including headers in the requests module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: We can add headers to requests module in Python by passing a dictionary of headers to the headers parameter of the requests.get() or requests.post() method.
---

**Contents**

[TOC]

# What is the Requests module in Python?

The `requests` module in Python is a third-party library used for sending HTTP requests using Python. In simpler terms, it allows you to send requests to a server and receive a response from it using Python code. This module is useful for accessing web APIs or scraping websites.

# What are headers in requests module?

Headers are an essential component of an HTTP request. The HTTP request headers contain additional information about the request being made. Headers provide additional metadata about the request or the client making the request. These headers are used to provide information such as User-Agent, Accept-Encoding, Referer, etc. 

# How to add headers to requests module in Python?

The requests module in Python makes it easy to add headers to a request. Within the request, you can add headers as a dictionary with key-value pairs. Here's an example of how to add headers to requests:

```python
import requests

headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3'}
response = requests.get('https://www.example.com', headers=headers)
```

In this example, the `User-Agent` is added as a header to the request with its value being the string provided. The `get` method is used to send a GET request to the URL specified with the headers added to the request. 

# Conclusion

To sum up, adding headers to requests in Python is as simple as specifying a dictionary of key-value pairs containing the headers you need. The requests module handles the rest, and you receive the response from the server based on the headers specified.
