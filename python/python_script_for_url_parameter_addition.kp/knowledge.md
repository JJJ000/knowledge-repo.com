---
title: Modify the url in Python by incorporating parameters
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can add params to a given URL in Python using the `requests` library with the `params` parameter.
---

**Contents**

[TOC]

## Introduction
In this tutorial, we will learn how to add parameters to a given URL in Python.

## Using the urllib.parse library
The urllib.parse library is the standard library for handling URLs in Python. We can use this library to add parameters to a given URL.

```python
from urllib.parse import urlencode

url = "https://example.com"
params = {"name": "John Doe", "age": 30}

url_with_params = url + "?" + urlencode(params)
print(url_with_params)
```

In this code snippet, we imported the `urlencode` function from the `urllib.parse` library. We then defined our URL and parameters and used the `urlencode` function to convert the parameters into a query string. We then appended the query string to the URL using the `+` operator.

## Using the requests library
The requests library is a popular library for making HTTP requests in Python. We can use this library to add parameters to a given URL.

```python
import requests

url = "https://example.com"
params = {"name": "John Doe", "age": 30}

response = requests.get(url, params=params)
url_with_params = response.url
print(url_with_params)
```

In this code snippet, we imported the `requests` library. We then defined our URL and parameters and used the `get` method of the `requests` library to make a GET request with the parameters. We then accessed the URL of the response object, which contains the URL with the parameters.

## Using the urljoin function
The `urljoin` function is a function from the urllib.parse library that can be used to join a base URL with a relative URL or a path. We can use this function to add parameters to a given URL.

```python
from urllib.parse import urljoin

base_url = "https://example.com"
path = "/users"
params = {"name": "John Doe", "age": 30}

url_with_params = urljoin(base_url+path, "?" + urlencode(params))
print(url_with_params)
```

In this code snippet, we imported the `urljoin` function from the `urllib.parse` library. We then defined our base URL, path, and parameters. We used the `urljoin` function to join the base URL and path and then append the query string to the resulting URL using the `+` operator.

## Conclusion
In this tutorial, we learned how to add parameters to a given URL in Python using three different approaches: the urllib.parse library, the requests library, and the urljoin function.
