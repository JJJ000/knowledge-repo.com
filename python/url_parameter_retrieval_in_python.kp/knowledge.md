---
title: Obtaining parameters from a url
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To retrieve parameters from a URL in Python, you can use the urllib.parse.parse\_qs() function.
---

**Contents**

[TOC]

Section 1: Introduction
Python is a widely used programming language that provides various libraries and modules to handle different types of functionalities. In the case of web development, Python offers a library known as 'urllib' that enables users to access various URL-related methods. In this tutorial, we will look into the process of retrieving parameters from a URL in Python.

Section 2: Retrieving Parameters from a URL using urllib.parse
The 'urllib.parse' library in Python provides various methods to parse URLs and retrieve their different components, including parameters. The following is an example demonstrating how to retrieve parameters from a URL.

```python
from urllib.parse import urlparse, parse_qs

url = "https://www.example.com/search?q=python&sort=relevance"

# Retrieving parameters from the URL
url_components = urlparse(url)
query_params = parse_qs(url_components.query)

# Accessing the parameters
print(query_params['q']) # Output: ['python']
print(query_params['sort']) # Output: ['relevance']
```

Section 3: Retrieving Parameters from a URL using Regular Expressions
Python also provides a method of retrieving parameters from a URL through Regular expressions. Regular expressions are a powerful tool used to match patterns in strings. The following is an example demonstrating how to retrieve parameters from a URL.

```python
import re

url = "https://www.example.com/search?q=python&sort=relevance"

# Pattern matching for query parameters
pattern = re.compile(r'\bq=([^&]*)')
matches = pattern.findall(url)

# Accessing the parameters
print(matches) # Output: ['python']

# Pattern matching for multiple query parameters
pattern2 = re.compile(r'\b(\w+)=([^&]*)')
matches2 = pattern2.findall(url)

# Accessing the parameters
print(dict(matches2)) # Output: {'q': 'python', 'sort': 'relevance'}
```

Section 4: Conclusion
In conclusion, Python provides various options to retrieve parameters from a URL. The 'urllib.parse' library can be used to parse URLs and retrieve their components. Regular expressions can also be used to extract patterns in strings, including parameters from URLs.
