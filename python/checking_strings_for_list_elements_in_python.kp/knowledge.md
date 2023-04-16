---
title: What is the syntax for determining if an item from a list is present in a string in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `in` operator to check if a string contains an element from a list.
---

**Contents**

[TOC]

**Section 1: Using `in` Operator** 

The `in` operator can be used to check if an element is present in a string. It returns a boolean value (`True` or `False`) depending on whether the element is present in the string.

For example, to check if the string `my_string` contains an element from the list `my_list`, we can use the following code:

```
if any(elem in my_string for elem in my_list):
    print('Element found')
else:
    print('Element not found')
```

**Section 2: Using `any()` Function**

The `any()` function can be used to check if any element of an iterable is `True`. It takes a list of boolean values (`True` or `False`) as an argument and returns `True` if any of the elements are `True`.

For example, to check if the string `my_string` contains an element from the list `my_list`, we can use the following code:

```
if any([elem in my_string for elem in my_list]):
    print('Element found')
else:
    print('Element not found')
```

**Section 3: Using `set()` Function**

The `set()` function can be used to convert a list into a set. A set is an unordered collection of unique elements. This can be used to check if an element is present in a string.

For example, to check if the string `my_string` contains an element from the list `my_list`, we can use the following code:

```
if set(my_list).intersection(my_string):
    print('Element found')
else:
    print('Element not found')
```

**Section 4: Using `count()` Function**

The `count()` function can be used to count the number of occurrences of an element in a string. It takes an element as an argument and returns the number of occurrences of that element in the string.

For example, to check if the string `my_string` contains an element from the list `my_list`, we can use the following code:

```
if any(my_string.count(elem) > 0 for elem in my_list):
    print('Element found')
else:
    print('Element not found')
```
