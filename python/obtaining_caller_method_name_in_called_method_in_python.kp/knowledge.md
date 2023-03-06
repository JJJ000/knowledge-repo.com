---
title: What is the way to obtain the name of the calling method within the called method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the inspect module in Python to get the caller`s method name in the called method.
---

**Contents**

[TOC]

## Introduction 

Python is a versatile language that can perform various activities with ease, including passing methods and functions. As a developer, it is essential to know the caller's method name to help in understanding the code's logic and its performance. In this article, we will discuss how to get the caller's method name in the called method in Python.

## Using the traceback module
The traceback module in Python provides us with a way of accessing the stack trace of a running program. We can use the `traceback.extract_stack()` function to extract the stack trace at the current point and then extract the function name from it.

```python
import traceback

def called_method():
    stack = traceback.extract_stack()
    filename, codeline, funcName, text = stack[-2]
    print("Method Name: ",funcName)
    
def caller_method():
    called_method()

caller_method()  
```

In the above code, we import the traceback module and define two methods, namely `caller_method` and `called_method`. In the `called_method`, we use the `traceback.extract_stack()` function to extract the current stack, which we then use to get the function name of the caller method.

## Looping over the stack frames
Another way of getting the caller's method name is by looping over the stack frames in the `inspect` module. The `inspect` module in Python provides us with a way of getting the stack frames of the running program, which we can loop over to find the caller's method name.

```python
import inspect

def called_method():
    stack = inspect.stack()
    frame, filename, line_num, func_name, source_code, source_index = stack[1]
    print("Method Name: ",func_name)

def caller_method():
    called_method()

caller_method()
```

In the above code, we import the `inspect` module and define two methods, namely `caller_method` and `called_method`. In the `called_method`, we use the `inspect.stack()` function to get the call stack of the running program, which we then loop over to get the method name of the caller method.

## Using sys._getframe
We can also use `sys._getframe()` to get the frame of the caller method and then extract its name.

```python
import sys

def called_method():
    frame = sys._getframe(1)
    print("Method Name: ", frame.f_code.co_name)

def caller_method():
    called_method()

caller_method()
```

In the above code, we define two methods, `caller_method` and `called_method`. In the `called_method`, we get the frame of the caller method using `sys._getframe(1)` and then extract its name using the `f_code.co_name`.

## Conclusion
In this article, we have discussed three methods of getting the caller's method name in the called method in Python. The traceback module, the inspect module, and the sys._getframe function are all excellent ways of finding the caller's method name.  All three functions can provide insightful information to help you understand the code's logic and its performance. Some developers may use these techniques to debug code or for profiling purposes.
