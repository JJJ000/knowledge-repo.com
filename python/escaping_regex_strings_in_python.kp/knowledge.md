---
title: Writing a string that is not interpreted as a regular expression
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use re.escape() to escape a string before using it in a regex.
---

**Contents**

[TOC]

### Using Raw Strings
Raw strings are strings that take all the characters literally, without any special treatment. To create a raw string, prefix the string with an 'r' or 'R'.

```python
import re

raw_string = r'\d+'
regex = re.compile(raw_string)
```

### Using Double Backslashes
Using double backslashes can also help you escape the special characters in a string.

```python
import re

escaped_string = '\\d+'
regex = re.compile(escaped_string)
```

### Using Regex Escape Function
The `re.escape()` function can be used to escape all the special characters in a string.

```python
import re

string = '\d+'
escaped_string = re.escape(string)
regex = re.compile(escaped_string)
```

### Using String Replace
The `string.replace()` function can be used to replace special characters with their escaped versions.

```python
import re

string = '\d+'
escaped_string = string.replace('\\', '\\\\')
regex = re.compile(escaped_string)
```
