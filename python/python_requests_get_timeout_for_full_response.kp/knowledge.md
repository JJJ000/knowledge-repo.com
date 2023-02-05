---
title: Time limit for obtaining the full response from a Python requests.get call
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The timeout for Python requests.get is the amount of time to wait for a server`s response before giving up.
---

**Contents**

[TOC]

1. Overview 
The requests module for Python allows for the making of HTTP requests to external servers from a Python script. The requests.get() function is used to make a GET request to a specific URL and retrieve the response from the server. The requests.get() function has an optional parameter, timeout, which allows the user to set a time limit for the request, after which the request will be aborted if the response is not received.

2. Syntax 
The syntax for the requests.get() function with the timeout parameter is as follows:

requests.get(url, timeout=timeout_value)

where url is the URL of the server to make the request to, and timeout_value is the time limit for the request, in seconds.

3. Example 
For example, to make a GET request to the URL http://www.example.com with a timeout of 10 seconds, the following code can be used:

response = requests.get("http://www.example.com", timeout=10)

4. Return Value
The return value of the requests.get() function with the timeout parameter is the entire response from the server, if the response is received within the time limit. If the response is not received within the time limit, the requests.get() function will return an error.
