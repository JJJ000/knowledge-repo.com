---
title: Separate elements by comma and remove whitespace in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the split() method with the parameter `, ` to split by comma and strip whitespace.
---

**Contents**

[TOC]

#### Using the `split()` Method

We can use the `split()` method to split a string into a list of strings by a given delimiter. The following example splits a string by a comma and strips the whitespace:

```python
my_string = "This,is,a,string"
my_list = my_string.split(",")

# Strip whitespace
my_list = [item.strip() for item in my_list]

print(my_list)
# Output: ['This', 'is', 'a', 'string']
```

#### Using the `split()` and `strip()` Methods

We can also use the `split()` and `strip()` methods together to achieve the same result. The following example splits a string by a comma and strips the whitespace:

```python
my_string = "This,is,a,string"
my_list = my_string.split(",").strip()

print(my_list)
# Output: ['This', 'is', 'a', 'string']
```

#### Using the `re.split()` Method

We can also use the `re.split()` method from the `re` module to split a string by a given delimiter. The following example splits a string by a comma and strips the whitespace:

```python
import re

my_string = "This,is,a,string"
my_list = re.split(",", my_string)

# Strip whitespace
my_list = [item.strip() for item in my_list]

print(my_list)
# Output: ['This', 'is', 'a', 'string']
```

#### Using the `str.split()` Method

We can also use the `str.split()` method to split a string by a given delimiter. The following example splits a string by a comma and strips the whitespace:

```python
my_string = "This,is,a,string"
my_list = str.split(my_string, ",")

# Strip whitespace
my_list = [item.strip() for item in my_list]

print(my_list)
# Output: ['This', 'is', 'a', 'string']
```
