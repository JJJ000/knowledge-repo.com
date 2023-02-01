---
title: What is the correct way to indent a multi-line string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Python uses indentation to denote the start and end of a multiline string, with each line of the string indented the same number of spaces.
---

**Contents**

[TOC]

#### Using Triple Quotes

When using triple quotes to create a multiline string, no indentation is necessary.

```python
my_string = """
This is a multiline string. 
It can span multiple lines.
"""
```

#### Using String Concatenation

When using string concatenation to create a multiline string, each line should be indented with the same amount of whitespace.

```python
my_string = "This is a multiline string.\n"
my_string += "It can span multiple lines."
```
