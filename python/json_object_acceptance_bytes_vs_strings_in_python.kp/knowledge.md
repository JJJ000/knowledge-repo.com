---
title: One possible rephrased sentence could be, "either allow the JSON object to process bytes or have urlopen produce string outputs."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Let urlopen output strings in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, JSON (JavaScript Object Notation) is a popular format used for exchanging data between a client and server. JSON can handle string values, numbers, booleans, arrays, and null, but not binary data. However, there can be scenarios where it might be necessary to encode or decode binary data as JSON. Another issue is that when using the urlopen function from the urllib module to open a URL, it always returns data in binary format. This leads to the question of whether JSON should accept bytes, or if there is a way to make urlopen output strings instead.

Section 2: JSON and Binary Data
JSON specification only supports strings, numbers, booleans, arrays, and null values, making it unable to handle binary data. However, Python has several built-in modules that can be used for encoding and decoding binary data into a format that can be placed within a JSON object. For instance, base64 and binascii modules can be used for encoding and decoding binary data into ASCII text format that can be placed within a JSON object. Though accepting bytes in JSON objects is not impossible, it may be unnecessary since encoding and decoding binary data is already available in Python.

Section 3: Using urlopen to output strings
When using the urlopen function from the urllib module, the output is always in binary format. However, it is possible to decode the data into a string format. One way to do this is by using the decode method of the bytes object. For instance:

```
from urllib import urlopen

response = urlopen('https://www.example.com')
html = response.read().decode('utf-8')
```

The decode() method is used to convert the binary data into a string format with the specified encoding. In this case, we're using utf-8 encoding.

Another way to handle this is to use Python's requests module. The requests module is popular among Python developers and includes a convenient way of parsing responses into JSON format. For instance:

```
import requests

response = requests.get('https://www.example.com')
json_response = response.json()
```

This method fetches the response from the website, and then the json() method is used to parse the response data into JSON format.

Section 4: Conclusion
Python provides several ways to encode and decode binary data, and there is no need to modify the JSON specification to accommodate bytes. When using urlopen, we can easily decode the binary data into strings without needing to modify the JSON object. Alternatively, we can consider using the requests module, which provides a convenient way of parsing responses into JSON format. Ultimately, there is no need to modify either the JSON object or urlopen methods for Python developers to work effectively with binary data in JSON format.
