---
title: What is the process of encoding a querystring using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the urllib.parse.quote() function to urlencode a querystring in Python.
---

**Contents**

[TOC]

# Using urllib.parse

The `urllib.parse` module provides functions for manipulating URLs and their component parts, to either break them down or build them up. The `urlencode()` function in this module can be used to urlencode a querystring in Python.

## Syntax

The syntax for using the `urlencode()` function is as follows:

```
urllib.parse.urlencode(query, doseq=False)
```

Where `query` is a dictionary or sequence of two-element tuples. The optional `doseq` argument is a boolean, which indicates whether to use the first value from sequences for the same key.

## Example

The following example shows how to use the `urlencode()` function to urlencode a querystring:

```
import urllib

query = {'q': 'Python Urlencode', 'lang': 'en'}
url = 'http://www.example.com/search?' + urllib.parse.urlencode(query)

print(url)
```

The output of the above code will be:

`http://www.example.com/search?q=Python+Urlencode&lang=en`
