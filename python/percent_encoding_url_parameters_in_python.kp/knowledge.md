---
title: What is the process for encoding url parameters as percent-encoded strings in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can percent-encode URL parameters in Python by using the urllib.parse.quote() function.
---

**Contents**

[TOC]

#### Using the urllib.parse Library

The `urllib.parse` library in Python contains a function called `quote()` which can be used to percent-encode URL parameters. The `quote()` function takes a string as an argument and returns a string with all non-alphanumeric characters replaced with a percent (%) sign followed by two hexadecimal digits.

```python
import urllib.parse

url = 'https://www.example.com/search?q=python'

encoded_url = urllib.parse.quote(url)
# https%3A%2F%2Fwww.example.com%2Fsearch%3Fq%3Dpython
```

#### Using the Requests Library

The `requests` library in Python also contains a function called `urlencode()` which can be used to percent-encode URL parameters. The `urlencode()` function takes a dictionary as an argument and returns a string with all the keys and values percent-encoded.

```python
import requests

params = {'q': 'python'}

encoded_params = requests.utils.urlencode(params)
# q=python
```

#### Using the String Replace Method

The `str.replace()` method can also be used to percent-encode URL parameters. The `str.replace()` method takes two arguments: the string to be replaced and the replacement string.

```python
url = 'https://www.example.com/search?q=python'

encoded_url = url.replace(' ', '%20')
# https://www.example.com/search?q=python
```
