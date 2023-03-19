---
title: Can you explain the meaning of "first-class" objects?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python, `first-class` objects refer to objects that can be assigned to variables, passed as arguments to functions, and returned as the result of a function call.
---

**Contents**

[TOC]

# Overview of First-Class Objects in Python

In Python, everything is an object. But not all objects are treated equally. Some objects are known as "first-class" objects, which means they have special privileges that allow them to be treated in a unique way.

# Definition of first-class objects in Python
 
First-class objects in Python are objects that can be assigned to variables, passed as arguments to functions, and returned as values from functions. They can be manipulated just like any other data type, such as integers or strings. 

# Examples of first-class objects in Python

There are many examples of first-class objects in Python, including integers, strings, lists, tuples, and objects created using custom classes. Here is an example of how integers can be treated as first-class objects:

```
def add(a, b):
    return a + b

x = 1
y = 2

result = add(x, y)

print(result) # Output: 3
```

In this example, the integers "1" and "2" are assigned to the variables "x" and "y" respectively, and then they are passed as arguments to the function "add". The function then returns the sum of the two integers, which is assigned to the variable "result". The fact that integers can be passed as arguments and returned as values makes them a first-class object in Python.
