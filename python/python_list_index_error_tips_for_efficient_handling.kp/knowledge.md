---
title: What is the most effective method for dealing with list.index() when the index may not exist in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use a try-except block to catch the ValueError exception that occurs when the item is not found in the list.
---

**Contents**

[TOC]

## Section 1: Understanding list.index()

`list.index()` is a built-in function in Python that returns the index of the first occurrence of an element in the given list. If the element is not found in the list, it raises a `ValueError`.

```python
my_list = ['apple', 'banana', 'orange']
index = my_list.index('banana')
print(index) # Output: 1
```

```python
my_list = ['apple', 'banana', 'orange']
try:
    index = my_list.index('mango')
    print(index)
except ValueError:
    print("Element not found in list")
```

## Section 2: Handling list.index(might-not-exist)

One way to handle the `list.index(might-not-exist)` scenario is to use a `try-except` block to catch the `ValueError` exception that is raised when the element is not found in the list. Here's an example:

```python
my_list = ['apple', 'banana', 'orange']
try:
    index = my_list.index('mango')
    print(index)
except ValueError:
    print("Element not found in list")
```

This will catch the `ValueError` and print "Element not found in list" instead of raising an error.

## Section 3: Using a default value

Another way to handle `list.index(might-not-exist)` is to use the `default` parameter of the `index()` method. This parameter specifies the value that is returned when the element is not found in the list. Here's an example:

```python
my_list = ['apple', 'banana', 'orange']
index = my_list.index('mango', default=-1)
print(index) # Output: -1
```

In this example, the `index()` method returns `-1` because the element `mango` is not found in the list.

## Section 4: Using the "in" operator

A third way to check if an element exists in a list is to use the `in` operator. The `in` operator returns `True` if the element is found in the list, and `False` otherwise. Here's an example:

```python
my_list = ['apple', 'banana', 'orange']
if 'mango' in my_list:
    index = my_list.index('mango')
    print(index)
else:
    print("Element not found in list")
```

This code first checks if the element `mango` is in the list using the `in` operator, and then prints the index of the element if it exists. If not, it prints "Element not found in list".
