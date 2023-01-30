---
title: What are the implications of using **kwargs?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: **kwargs is a keyword argument dictionary used to pass an arbitrary number of keyword arguments to a function in Python.
---

**Contents**

[TOC]

#### Definition
**kwargs stands for keyword arguments and is a special syntax in Python used to pass a non-keyworded, variable-length argument list. It allows us to pass the variable number of keyword arguments to a function.

#### Usage
**kwargs is used when we want to handle named arguments in a function. When we call a function with some keyword arguments, then the function can use the **kwargs to pass the keyword arguments as a dictionary. The **kwargs can be used to pass keyworded arguments to a function with the help of the double asterisk. 

#### Syntax
The syntax of **kwargs is as follows:

def function_name(**kwargs):
    # body of the function

#### Example
For example, if we have a function that takes two arguments, a and b, and we want to pass three arguments to it, we can use **kwargs to do so. 

def add_numbers(a, b, **kwargs):
    # body of the function
    return a + b + kwargs['c']

add_numbers(1, 2, c=3)  # returns 6
