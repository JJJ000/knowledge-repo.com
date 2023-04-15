---
title: To utilize numerous arguments, provide a list as input to a function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the asterisk (*) operator to pass a list as multiple arguments to a function.
---

**Contents**

[TOC]

## Introduction
In Python, it's possible to pass a list to a function to act as multiple arguments. This is useful if you have a function that expects multiple arguments, but you want to pass those arguments in a more concise way.

## Example
Let's say we have a function that takes three arguments:

```python
def foo(bar, baz, qux):
    print(bar, baz, qux)
```

Instead of calling this function with three separate arguments, we can pass a list of arguments:

```python
args = ['hello', 'world', 123]
foo(*args)
```

Here, we use the `*` operator to unpack the list and pass its values as separate arguments to the function.

## Using the *args syntax
The `*args` syntax can be used to pass a variable number of arguments to a function. Here's an example:

```python
def foo(*args):
    for arg in args:
        print(arg)

foo(1, 2, 3, 4, 5)
```

This will output:

```
1
2
3
4
5
```

## Conclusion
Passing a list to a function to act as multiple arguments can be a useful technique in Python, especially when dealing with functions that expect a large number of arguments. By using the `*` operator or the `*args` syntax, we can pass our arguments in a more concise way.
