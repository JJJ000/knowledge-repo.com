---
title: What is the quickest method to determine if an element is present in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Using the `in` operator is the fastest way to check if a value exists in a list in Python.
---

**Contents**

[TOC]

**Using the "in" Operator:**

The most efficient way to check if a value exists in a list in Python is to use the "in" operator. This operator checks if a value is present in a list and returns a boolean value (True or False) based on the result.

**Example:**

```python
list = [1, 2, 3, 4, 5]

if 3 in list:
  print("Value found in list")

# Output: Value found in list
```

**Using the "index" Method:**

Another way to check if a value exists in a list is to use the "index" method. This method returns the index of the first occurrence of a value in a list. If the value is not present, it returns a ValueError.

**Example:**

```python
list = [1, 2, 3, 4, 5]

try:
  index = list.index(3)
  print("Value found at index:", index)
except ValueError:
  print("Value not found in list")

# Output: Value found at index: 2
```

**Using the "count" Method:**

The "count" method can also be used to check if a value exists in a list. This method returns the number of occurrences of a value in a list. If the value is not present, it returns 0.

**Example:**

```python
list = [1, 2, 3, 4, 5]

count = list.count(3)

if count > 0:
  print("Value found in list")
else:
  print("Value not found in list")

# Output: Value found in list
```
