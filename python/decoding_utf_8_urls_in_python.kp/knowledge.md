---
title: Decode a utf-8 encoded url using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the urllib.parse.unquote() function to URL decode UTF-8 in Python.
---

**Contents**

[TOC]

# Section 1: Overview

URL decoding is the process of converting URL encoded strings into their original form. In Python, URL decoding can be done using the urllib.parse module, which provides functions for URL encoding and decoding.

# Section 2: UTF-8

UTF-8 is a character encoding standard that is used for encoding Unicode characters. It is the most common encoding used on the web and is supported by all major browsers.

# Section 3: Python urllib.parse

The Python urllib.parse module provides functions for URL encoding and decoding. The unquote() function can be used to decode a URL encoded string in UTF-8. This function takes a single parameter, which is the URL encoded string to be decoded.

# Section 4: Example

For example, the following code can be used to decode a URL encoded string in UTF-8:

```python
import urllib.parse

url_encoded_string = "Hello%20World"
decoded_string = urllib.parse.unquote(url_encoded_string)

print(decoded_string) # Outputs "Hello World"
```
