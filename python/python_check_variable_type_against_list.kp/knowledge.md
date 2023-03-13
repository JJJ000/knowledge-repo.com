---
title: How to determine if a variable in Python is of any type in a given list using isinstance()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the any() function to check if the variable is an instance of any of the types in the list using a generator expression.
---

**Contents**

[TOC]

# Introduction

In Python, we can check if a variable is an instance of a specific type using the `isinstance()` function. However, what if we want to check if a variable is an instance of any of the types in a list? In this tutorial, we will discuss how to do that in Python.

# Using isinstance() with a tuple of types

One way to check if a variable is an instance of any type in a list is to create a tuple of types and use the `isinstance()` function with the variable and the tuple. Here is an example:

```python
num = 10
types = (int, float, complex)
if isinstance(num, types):
    print("num is an instance of either int, float, or complex")
```

In the example above, `num` is an integer, and we want to check if it is an instance of any of the types in the `types` tuple. We use the `isinstance()` function with `num` and `types`, and if the result is `True`, we print a message indicating that `num` is an instance of either `int`, `float`, or `complex`.

# Using any() with a list comprehension

Another way to check if a variable is an instance of any type in a list is to use `any()` with a list comprehension. Here is an example:

```python
num = 10
types = [int, float, complex]
if any([isinstance(num, t) for t in types]):
    print("num is an instance of either int, float, or complex")
```

In this example, we use a list comprehension to create a list of `True` and `False` values, where each value indicates if `num` is an instance of the corresponding type in the `types` list. We then use `any()` with this list of values, which returns `True` if any of the values are `True`, indicating that `num` is an instance of any of the types in the `types` list.

# Using set intersection

A third way to check if a variable is an instance of any type in a list is to use set intersection. Here is an example:

```python
num = 10
types = [int, float, complex]
if set([type(num)]).intersection(types):
    print("num is an instance of either int, float, or complex")
```

In this example, we first create a set containing the type of `num`. We then create another set containing the types in the `types` list. We use the `intersection()` method of the set containing the type of `num` with the set containing the types in the `types` list to get a new set containing only the types that are common to both sets. If this new set is not empty, it means that `num` is an instance of at least one of the types in the `types` list. We then print a message indicating this. 

# Conclusion

In this tutorial, we discussed three ways to check if a variable is an instance of any type in a list in Python. These include using `isinstance()` with a tuple of types, using `any()` with a list comprehension, and using set intersection. These methods are useful when we want to check if a variable can have different types, but we don't want to write separate code for each type.
