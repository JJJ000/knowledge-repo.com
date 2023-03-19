---
title: What is the process of checking whether a url in Python is valid or not, including malformed urls?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use urlparse from the urllib.parse library to validate a URL in Python.
---

**Contents**

[TOC]

## 1. Using urllib.parse library

Python's urllib.parse module is a useful library for parsing URLs. It can be used to validate the URL and check if it is well-formed or not. The URL is parsed into its different components such as scheme, netloc, path, etc., and these components are checked for validity. 

```python
from urllib.parse import urlparse

url = "https://www.google.com/search?q=python"
parsed = urlparse(url)

if all([parsed.scheme, parsed.netloc]):
    print("Valid URL")
else:
    print("Invalid URL")
```

In the above code, the `urlparse()` method is used to parse the URL into its components. The `scheme` and `netloc` components of the URL are checked for validity. If they are present, it is considered a valid URL.

## 2. Using validators library

The validators library is a Python package that provides a set of functions to validate various types of data, including URLs. It provides several functions to validate the URL such as `url()`, `urlsafe()`, `domain()`, etc.

```python
import validators

url = "https://www.google.com/search?q=python"

if validators.url(url):
    print("Valid URL")
else:
    print("Invalid URL")
```

In the above code, the `url()` function from the validators library is used to validate the URL. It returns True if the URL is valid, otherwise False. 

## 3. Using regex

Regular expressions are powerful tools for pattern matching and can be used to validate a URL as well. A regex pattern can be created to match the different components of a URL and checked for validity. 

```python
import re

url = "https://www.google.com/search?q=python"

url_pattern = re.compile(
    r'^(?:http|ftp)s?://' # scheme
    r'(?:(?:[A-Z0-9](?:[A-Z0-9-]{0,61}[A-Z0-9])?\.)+(?:[A-Z]{2,6}\.?|[A-Z0-9-]{2,}\.?)|' # domain
    r'localhost|' # localhost
    r'\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})' # IP
    r'(?::\d+)?' # port
    r'(?:/?|[/?]\S+)$', re.IGNORECASE)

if url_pattern.match(url):
    print("Valid URL")
else:
    print("Invalid URL")
```

In the above code, a regex pattern is created using regular expression syntax to match the different components of a URL. The `match()` method of the regex pattern is used to check if the URL matches the pattern. 

## 4. Using urlparse library

Another method to validate a URL is to use the urlparse module from the Python standard library. The urlparse module provides several functions to check if the URL is well-formed or not.

```python
from urllib.parse import urlparse

url = "https://www.google.com/search?q=python"

try:
    result = urlparse(url)
    if result.scheme and result.netloc:
        print("Valid URL")
    else:
        print("Invalid URL")
except ValueError:
    print("Invalid URL")
```

In the above code, the `urlparse()` method is used to parse the URL and the `scheme` and `netloc` components are checked for validity. If the URL is not well-formed or contains invalid components, a `ValueError` exception will be raised which can be caught to handle the error.
