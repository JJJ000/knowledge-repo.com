---
title: Use a Python script to send a file through post
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To send a file using POST from a Python script, use the requests library to make an HTTP POST request with the file as the request body.
---

**Contents**

[TOC]

## Introduction
Python provides several libraries to interact with web services. One of the most commonly used libraries to interact with web services is the `requests` library. In this guide, we will learn how to use the `requests` library to send files using POST method from a Python script.


## Installing requests library
Before we can start using the `requests` library, we need to install it. We can install `requests` library using pip, which is the package installer for Python.

To install this package from the command line, run the following command:

`pip install requests`


## Sending file using POST method
We can use the `requests.post()` method to send a file using POST method from a Python script. The method requires the URL of the web service, and the path of the file to be sent.

Here is an example code that sends a file using POST method:

```
import requests

url = "https://example.com/upload"
file_path = "/path/to/myfile.txt"

with open(file_path, "rb") as f:
    files = {"file": f}
    response = requests.post(url, files=files)

print(response.status_code)
```

In the above code, we have imported the `requests` library and defined the URL of the web service and the path of the file to be sent.

We have then opened the file in binary mode and created a dictionary containing the file with the key name `file`.

Finally, we have sent the file using POST method using the `requests.post()` method and printed the status code of the response.

## Conclusion
In this guide, we have learned how to use the `requests` library to send files using POST method from a Python script. We first installed the `requests` library and then used the `requests.post()` method to send files. This method requires the URL of the web service, and the path of the file to be sent, and returns the response from the web service.
