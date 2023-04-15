---
title: What is the method for determining if a variable is a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can check if the type of a variable is a string by using the type() function and comparing the result to the type `str`.
---

**Contents**

[TOC]

# Checking Type of a Variable

## Using type()

The `type()` function can be used to check the type of a variable in Python. For example:

```
my_var = "Hello World"
print(type(my_var))
```

The output of this code will be `<class 'str'>`, indicating that the type of `my_var` is a string.

## Using isinstance()

The `isinstance()` function can also be used to check the type of a variable in Python. For example:

```
my_var = "Hello World"
print(isinstance(my_var, str))
```

The output of this code will be `True`, indicating that the type of `my_var` is a string.
