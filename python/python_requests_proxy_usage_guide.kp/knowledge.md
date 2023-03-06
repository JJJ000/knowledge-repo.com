---
title: Using the Python 'requests' module to create proxies
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The `Requests` module in Python can use proxies by specifying the proxy parameter in the HTTP requests.
---

**Contents**

[TOC]

Section 1: Introduction to Proxies

Proxies act as intermediaries between a user and the internet. They are a type of server that can be used to hide the user's IP address and location. This can be useful when attempting to access websites or information that are restricted or blocked in specific regions. In this context, Python 'Requests' module is often used to make HTTP requests and communicate with web servers.

Section 2: Using Proxies with Python 'Requests' Module

Python 'Requests' module supports the use of proxies by passing an additional parameter to the 'get' or 'post' functions. The parameter specifies the host and port number of the proxy server.

Here is an example:

```python
import requests

proxy = {
    'http': 'http://username:password@proxyserver:port',
    'https': 'https://username:password@proxyserver:port'
}

response = requests.get('https://www.example.com', proxies=proxy)

print(response.status_code)
```

In this example, the proxy dictionary contains the URLs for the HTTP and HTTPS endpoints of the proxy server. The proxy server requires authentication, so the username and password are provided in the URL.

Section 3: Handling Exceptions

When using proxies, it is important to handle exceptions that may occur. If the proxy fails to respond or there is an authentication error, the request will fail.

The 'requests' module provides a number of exceptions that can be caught, such as Timeout, ProxyError, and SSLError. Here is an example of catching a ProxyError exception:

```python
import requests

proxy = {'https': 'https://proxyserver:port'}

try:
    response = requests.get('https://www.example.com', proxies=proxy)
    print(response.status_code)
except requests.exceptions.ProxyError as e:
    print("Proxy Error:", e)
```

In this example, the 'try' block attempts the HTTP request. If a ProxyError occurs, the exception is caught and a message is printed to the console.

Section 4: Conclusion

Python 'Requests' module is a powerful tool for web scraping and HTTP requests. With the ability to use proxies, the module can be used to bypass restrictions and access information that might otherwise be unavailable. Handling exceptions is an important consideration when using proxies, as there may be times when the proxy server is unavailable or there is an authentication issue.
