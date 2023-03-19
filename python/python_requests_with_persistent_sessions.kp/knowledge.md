---
title: Persistent sessions and Python requests
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python Requests module allows the creation of persistent sessions which enables a user to send multiple requests using the same connection.
---

**Contents**

[TOC]

## Introduction to Python Requests

Python Requests is a popular HTTP client library that allows you to send HTTP/1.1 requests extremely easily. Requests is a simple and elegant Python library that makes it easy to work with HTTP/1.1 requests and responses. It is built on top of urllib3, which is another Python HTTP client library. Requests's simple and easy-to-use API allows you to send HTTP requests and retrieve responses with just a few lines of code. 

## What is a Persistent Session?

In a web application, a session is created once a user logs in or signs up. Session data is transferred between the browser and the server each time a user interacts with the web application. A persistent session, also known as a persistent cookie, is a cookie that is stored on the client-side for a specific period of time. This cookie allows the user to remain logged in for an extended amount of time, even if they close their browser or shut down their computer.

## How to Create a Persistent Session in Python Requests?

Creating a persistent session with Python Requests is easy. All you need to do is create a session object using the requests.Session() method. Once you have the session object, you can make a GET or POST request just as you would with a normal requests object. The session object will automatically handle cookies for you, so any cookies sent by the server will be stored in the session object and passed back with subsequent requests.

## Example of Using Persistent Session in Request

Here is an example of how to create a persistent session in Python Requests:

```python
import requests

# Create a persistent session
session = requests.Session()

# Set a custom header
headers = {'User-Agent': 'Mozilla'}

# Send a GET request using the session
response = session.get('https://google.com', headers=headers)

# Close the session
session.close()
```

In this example, we create a persistent session with `requests.Session()`. We set a custom header with the `headers` argument, and then send a GET request using the session's `get()` method. Any cookies that are set by the server in the response headers will be stored in the session object and sent back with subsequent requests made using this session. Finally, we close the session with `session.close()`.
