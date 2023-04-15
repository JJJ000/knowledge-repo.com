---
title: What is the process for converting a string to uppercase?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the upper() method to change a string into uppercase in Python.
---

**Contents**

[TOC]

# Using the Upper Method

The `upper()` method can be used to convert a string to uppercase.

```python
string = "this is a string"
string.upper()
```

This will return `"THIS IS A STRING"`.

# Using the String Formatting Operator

The `%s` string formatting operator can also be used to convert a string to uppercase.

```python
string = "this is a string"
"%s" % string.upper()
```

This will return `"THIS IS A STRING"`.

# Using the String Replace Method

The `replace()` method can also be used to convert a string to uppercase.

```python
string = "this is a string"
string.replace("this is a string", string.upper())
```

This will return `"THIS IS A STRING"`.
