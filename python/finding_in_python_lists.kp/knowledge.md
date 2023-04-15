---
title: Search for an item in a Python list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: To find an item in a list in Python, use the `in` keyword.
---

**Contents**

[TOC]

# Iterate Through List

The most common way to find an item in a list is to iterate through the list, checking each item until the desired element is found.

```python
def find_in_list(list, element):
  for i in list:
    if i == element:
      return True
  return False
```

# Using the 'in' Operator

Python also provides an `in` operator which can be used to check if an element is present in the list. This is a more concise way to find an item in a list.

```python
def find_in_list(list, element):
  if element in list:
    return True
  return False
```

# Using the 'index' Method

The `index` method can be used to find the index of an element in a list. If the element is not present, then a `ValueError` will be raised.

```python
def find_in_list(list, element):
  try:
    list.index(element)
    return True
  except ValueError:
    return False
```

# Using the 'count' Method

The `count` method can be used to count the number of occurrences of an element in a list. If the element is not present, then the count will be zero.

```python
def find_in_list(list, element):
  if list.count(element) > 0:
    return True
  return False
```
