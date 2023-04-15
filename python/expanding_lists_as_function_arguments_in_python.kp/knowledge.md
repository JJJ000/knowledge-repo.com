---
title: How can a list be converted into function arguments in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `asterisk` (*) operator to expand a list into function arguments.
---

**Contents**

[TOC]

## Introduction
Sometimes we have a list of values that we want to pass as arguments to a function. One way to pass these arguments is to use the `*` operator to unpack the list. This is known as expanding a list into function arguments. In this tutorial, we will see how to expand a list into function arguments in Python.

## Example
Let's say we have a function that takes three arguments:

```python
def my_func(arg1, arg2, arg3):
    print(arg1)
    print(arg2)
    print(arg3)
```

And we have a list of three values:

```python
my_list = [1, 2, 3]
```

We can expand this list into function arguments by adding the `*` operator before the list:

```python
my_func(*my_list)
```

This will output the following:

```
1
2
3
```

## Explanation
Adding the `*` operator before a list unpacks it and passes its elements as separate arguments to the function. In our example, the list `my_list` was expanded into three separate arguments: `1, 2, 3`. These were then passed to `my_func` as `arg1`, `arg2`, and `arg3`, respectively.

## Conclusion
Expanding a list into function arguments is a useful feature of Python that allows us to pass a variable number of arguments to a function. It can save us time and ensure that our code is more concise and readable.
