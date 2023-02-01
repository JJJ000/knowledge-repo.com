---
title: What is the most straightforward way to get rid of multiple spaces in a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, use the replace() method to replace multiple spaces with a single space.
---

**Contents**

[TOC]

### Solution 1:
Using the `replace()` Method

The `replace()` method can be used to remove multiple spaces from a string in Python. This method takes two parameters: the string to be replaced and the string to replace it with. To remove multiple spaces, simply pass two empty strings as parameters.

For example: 

```
my_string = "This   is   a   string  with   multiple   spaces"
my_string.replace(" ", "")
```

The output of this code will be: `Thisisastringwithmultiplespaces`.

### Solution 2:
Using Regular Expressions

Regular expressions can also be used to remove multiple spaces from a string in Python. The `re.sub()` method takes three parameters: the pattern to be matched, the string to replace it with, and the string to be searched. To remove multiple spaces, simply pass a regular expression pattern that matches one or more spaces and an empty string as the replacement string.

For example:

```
import re
my_string = "This   is   a   string  with   multiple   spaces"
re.sub(r"\s+", "", my_string)
```

The output of this code will be: `Thisisastringwithmultiplespaces`.
