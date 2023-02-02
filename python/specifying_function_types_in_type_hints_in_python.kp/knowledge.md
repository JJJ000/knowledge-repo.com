---
title: What type of function should I indicate in my type hints?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can specify the function type by using the `Callable` type hint.
---

**Contents**

[TOC]

**Section 1: Function Types**

Function types refer to the types of functions that can be used in Python. There are a variety of function types, including built-in functions, user-defined functions, and lambda functions. 

**Section 2: Type Hints**

Type hints are a way to provide type information about a variable or function. They are used to help the Python interpreter understand the types of values that a function is expecting to receive and the types of values it should return. 

**Section 3: Specifying Function Types**

When specifying function types in type hints, the syntax is similar to the syntax for specifying variable types. The type of the function is specified in parentheses after the name of the function. For example, if a function is expected to return an integer, the type hint would be written as:

`def my_function() -> int:`

**Section 4: Examples**

Here are some examples of how to specify different types of functions in type hints:

* A function that returns an integer: `def my_function() -> int:`
* A function that takes two arguments and returns a float: `def my_function(arg1, arg2) -> float:`
* A lambda function that takes a list and returns a list of strings: `lambda my_list: -> [str]:`
