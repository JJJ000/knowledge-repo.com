---
title: Record every request made using the python-requests module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To log all requests from the python-requests module, you can use a logger and set the level to DEBUG.
---

**Contents**

[TOC]

## Introduction

The `python-requests` module is a popular library for making HTTP requests in Python. While the library is easy to use and provides a lot of functionality, it can be difficult to debug or troubleshoot when requests fail or behave unexpectedly. One approach is to log all requests made by the `requests` module. In this tutorial, we will discuss several ways to achieve this.

## Using the Requests Event Hooks

The `requests` module provides a mechanism for registering event hooks that are called during various stages of the request-response cycle. By registering an event hook for the `request` event, we can log details about the request that is being made. Here is an example:

```python
import requests

def log_request(request, *args, **kwargs):
    print(f"Request: {request.url}")
    print(f"\tMethod: {request.method}")
    print(f"\tHeaders: {request.headers}")
    print(f"\tBody: {request.body}")

requests.on_request(log_request)

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
```

In this example, we define a function `log_request` that prints details about the request. We then register this function as an event hook using the `on_request` method. When we make a request using the `requests` module, the `log_request` function will be called with details about the request.

## Using a Custom Request Session

Another approach is to create a custom subclass of `requests.Session` that overrides the `send` method. This method is responsible for actually sending the request and receiving the response. By logging information about the request before it is sent, we can effectively log all requests made using our custom session. Here is an example:

```python
import requests

class LoggingSession(requests.Session):
    def send(self, request, **kwargs):
        # Log the request details
        print(f"Request: {request.url}")
        print(f"\tMethod: {request.method}")
        print(f"\tHeaders: {request.headers}")
        print(f"\tBody: {request.body}")

        # Actually send the request and get the response
        response = super().send(request, **kwargs)

        # Log the response details
        print(f"Response: {response.url}")
        print(f"\tStatus Code: {response.status_code}")
        print(f"\tHeaders: {response.headers}")
        print(f"\tBody: {response.text}")

        return response

# Create a custom session to log requests
session = LoggingSession()

# Use the custom session to make requests
response = session.get("https://jsonplaceholder.typicode.com/posts/1")
```

In this example, we create a subclass of `requests.Session` called `LoggingSession`. We override the `send` method to log information about the request and response. We then create an instance of our custom session and use it to make requests. All requests made using this session will be logged.

## Using a Third-Party Library

Finally, there are several third-party libraries available for logging requests made by the `requests` module. One popular library is `httptracer`. Here is an example:

```python
import requests
from httptracer import trace_requests

# Enable HTTP tracing
trace_requests()

# Make some requests
response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
```

In this example, we import the `trace_requests` function from the `httptracer` library. This function enables tracing for all requests made by the `requests` module. When we make a request using the `requests` module, details about the request and response will be logged automatically.
