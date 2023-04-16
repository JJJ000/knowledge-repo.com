---
title: Retrieving the names of parameters within a Python function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The parameter names of a Python function can be accessed using the function`s `.\_\_code\_\_.co\_varnames` attribute.
---

**Contents**

[TOC]

# Section 1: Using dir() 

The `dir()` function can be used to get a list of parameter names inside a python function. This function takes an object as an argument and returns a list of valid attributes of the object.

# Section 2: Using inspect.getfullargspec() 

The `inspect.getfullargspec()` function can be used to get a list of parameter names inside a python function. This function takes a function object as an argument and returns a `FullArgSpec` object which contains a list of parameter names.

# Section 3: Using inspect.signature() 

The `inspect.signature()` function can be used to get a list of parameter names inside a python function. This function takes a function object as an argument and returns a `Signature` object which contains a list of parameter names.

# Section 4: Using inspect.getargspec() 

The `inspect.getargspec()` function can be used to get a list of parameter names inside a python function. This function takes a function object as an argument and returns a `ArgSpec` object which contains a list of parameter names.
