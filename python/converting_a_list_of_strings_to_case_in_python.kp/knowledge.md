---
title: Change all the strings in a list to either lowercase or uppercase
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert a list with strings to lowercase, use the list comprehension syntax [string.lower() for string in list], and to convert a list with strings to uppercase, use the list comprehension syntax [string.upper() for string in list].
---

**Contents**

[TOC]

# Lowercase

To convert a list of strings to lowercase, use the `lower()` method on each string in the list.

Example:
```python
list_of_strings = ["Hello", "World"]

lowercase_list = [string.lower() for string in list_of_strings]

# lowercase_list = ["hello", "world"]
```

# Uppercase

To convert a list of strings to uppercase, use the `upper()` method on each string in the list.

Example:
```python
list_of_strings = ["Hello", "World"]

uppercase_list = [string.upper() for string in list_of_strings]

# uppercase_list = ["HELLO", "WORLD"]
```
