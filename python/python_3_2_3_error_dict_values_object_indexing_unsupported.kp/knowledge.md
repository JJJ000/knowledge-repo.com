---
title: When using Python 3.2.3, you may encounter a typeerror 'dict_values' object does not support indexing
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The error message indicates that you cannot directly index into a dictionary`s values in Python 3.2.3, as they are returned as a dictionary view object instead of a list.
---

**Contents**

[TOC]

1. Problem Explanation: 

The error message "TypeError: 'dict_values' object does not support indexing" in Python 3.2.3 is usually encountered when trying to access an element in a dictionary's values view using index notation. 

2. Reason for the Error: 

In Python 3.2.3, calling the `values()` method on a dictionary returns a dictionary view object that provides a dynamic view on the dictionary's values. This view behaves like a set, which means that it does not support indexing or slicing. 

3. Solution: 

The correct way to access values from a dictionary view in Python 3.2.3 is to iterate over them using a for loop or use one of the many built-in functions that accept iterable objects as arguments. Some commonly used ones are `list()`, `tuple()`, and `set()`, which can convert the dictionary view object into their respective data structures. Alternatively, you can upgrade to a newer version of Python that supports indexing on dictionary view objects. 

Example code:

```
# create a dictionary
my_dict = {'a': 1, 'b': 2, 'c': 3}

# get the dictionary view object
values_view = my_dict.values()

# iterate over the dictionary view object
for val in values_view:
    print(val)

# convert the view object to a list
values_list = list(values_view)

# access the second value using indexing on the list
second_val = values_list[1]
print(second_val)
```

4. Upgrade to a newer version:

If you prefer to use indexing notation with dictionary views, you can upgrade to a newer version of Python that supports it. As of Python 3.7, indexing and slicing are allowed on dictionary views, which means that you can access individual items in the view using the same notation as with lists or tuples.

Example code:

```
# create a dictionary
my_dict = {'a': 1, 'b': 2, 'c': 3}

# get the dictionary view object
values_view = my_dict.values()

# access the second value using indexing
second_val = values_view[1]
print(second_val)
```
