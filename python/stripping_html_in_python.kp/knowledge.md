---
title: Remove html tags from strings in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `strip\_tags` function from the `html` module to strip HTML from strings in Python.
---

**Contents**

[TOC]

### Using Regular Expressions
Regular expressions can be used to strip HTML tags from a string by using the `re.sub()` function. The following code snippet shows an example of how this can be done:

```
import re

html_string = "<h1>Hello World!</h1>"

clean_string = re.sub('<[^<]+?>', '', html_string)

print(clean_string)

# Output: Hello World!
```

### Using BeautifulSoup
BeautifulSoup is a Python library used for parsing HTML and XML documents. It can be used to strip HTML tags from a string by using the `.get_text()` method. The following code snippet shows an example of how this can be done:

```
from bs4 import BeautifulSoup

html_string = "<h1>Hello World!</h1>"

soup = BeautifulSoup(html_string, 'html.parser')

clean_string = soup.get_text()

print(clean_string)

# Output: Hello World!
```

### Using lxml
lxml is a Python library used for processing XML and HTML documents. It can be used to strip HTML tags from a string by using the `.text_content()` method. The following code snippet shows an example of how this can be done:

```
from lxml.html import fromstring

html_string = "<h1>Hello World!</h1>"

tree = fromstring(html_string)

clean_string = tree.text_content()

print(clean_string)

# Output: Hello World!
```

### Using html.parser
The `html.parser` module is part of the Python standard library and can be used to strip HTML tags from a string by using the `.unescape()` method. The following code snippet shows an example of how this can be done:

```
import html

html_string = "<h1>Hello World!</h1>"

clean_string = html.unescape(html_string)

print(clean_string)

# Output: Hello World!
```
