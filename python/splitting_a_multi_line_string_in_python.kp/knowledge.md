---
title: What is the best way to divide a multi-line string into separate lines?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the string`s splitlines() method to split a multi-line string into multiple lines.
---

**Contents**

[TOC]

**Using the Split() Method**

The `split()` method can be used to split a multi-line string into multiple lines. It takes a string as an argument and returns a list of strings.

Example:
```python
my_string = "This is a multi-line string.\nIt has multiple lines.\nIt can be split into multiple lines."

lines = my_string.split("\n")
print(lines)
```
Output:
```
['This is a multi-line string.', 'It has multiple lines.', 'It can be split into multiple lines.']
```

**Using the Regex Library**

The `re` (regular expressions) library in Python can be used to split a multi-line string into multiple lines. The `split()` method can be used to split the string based on a given pattern. 

Example:
```python
import re

my_string = "This is a multi-line string.\nIt has multiple lines.\nIt can be split into multiple lines."

lines = re.split("\n", my_string)
print(lines)
```
Output:
```
['This is a multi-line string.', 'It has multiple lines.', 'It can be split into multiple lines.']
```

**Using the For Loop**

A `for` loop can be used to split a multi-line string into multiple lines. The `splitlines()` method can be used to split the string into a list of strings. 

Example:
```python
my_string = "This is a multi-line string.\nIt has multiple lines.\nIt can be split into multiple lines."

lines = my_string.splitlines()

for line in lines:
    print(line)
```
Output:
```
This is a multi-line string.
It has multiple lines.
It can be split into multiple lines.
```

**Using the List Comprehension**

The list comprehension can be used to split a multi-line string into multiple lines. The `splitlines()` method can be used to split the string into a list of strings. 

Example:
```python
my_string = "This is a multi-line string.\nIt has multiple lines.\nIt can be split into multiple lines."

lines = [line for line in my_string.splitlines()]
print(lines)
```
Output:
```
['This is a multi-line string.', 'It has multiple lines.', 'It can be split into multiple lines.']
```
