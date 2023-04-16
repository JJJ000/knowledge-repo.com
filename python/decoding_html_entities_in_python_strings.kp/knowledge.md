---
title: How can I convert html entities to their corresponding characters in a Python string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the html.unescape() method to decode HTML entities in a Python string.
---

**Contents**

[TOC]

#### Using HTMLParser

The HTMLParser module can be used to decode HTML entities in a Python string.

```python
import html.parser

parser = html.parser.HTMLParser()

html_string = '&lt;a href="http://www.example.com"&gt;Example&lt;/a&gt;'

decoded_string = parser.unescape(html_string)

print(decoded_string)

# <a href="http://www.example.com">Example</a>
```

#### Using html.unescape

The html.unescape() function can also be used to decode HTML entities in a Python string.

```python
import html

html_string = '&lt;a href="http://www.example.com"&gt;Example&lt;/a&gt;'

decoded_string = html.unescape(html_string)

print(decoded_string)

# <a href="http://www.example.com">Example</a>
```

#### Using Regular Expressions

Regular expressions can also be used to decode HTML entities in a Python string.

```python
import re

html_string = '&lt;a href="http://www.example.com"&gt;Example&lt;/a&gt;'

decoded_string = re.sub(r'&([^;]*);', lambda m: chr(int(m.group(1), 16)), html_string)

print(decoded_string)

# <a href="http://www.example.com">Example</a>
```

#### Using BeautifulSoup

The BeautifulSoup library can also be used to decode HTML entities in a Python string.

```python
from bs4 import BeautifulSoup

html_string = '&lt;a href="http://www.example.com"&gt;Example&lt;/a&gt;'

soup = BeautifulSoup(html_string, 'html.parser')

decoded_string = soup.get_text()

print(decoded_string)

# <a href="http://www.example.com">Example</a>
```
