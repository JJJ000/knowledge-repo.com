---
title: How to obtain the name of the calling function within a Python function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the `inspect` module in Python to get the caller function name inside another function.
---

**Contents**

[TOC]

## Introduction

Sometimes, it is useful to retrieve the caller function name inside another function in Python. This can be done using the inspect module. In this article, we will go through the steps to achieve this.

## Step 1: Import the Inspect module

The first step is to import the inspect module in our Python script.

```python
import inspect
```

## Step 2: Use the Inspect module to retrieve the Caller Function Name

Once we have imported the inspect module, we can use the `stack()` function to get the caller function name.

```python
def function1():
    function2()
    
def function2():

    caller_function_name = inspect.stack()[1][3]
    
    print(caller_function_name)
    
function1()
```

Here, we have two functions - `function1()` and `function2()`. `function1()` calls `function2()`. In `function2()`, we use the `inspect.stack()` function to retrieve the caller function name, which is `function1()`.

## Step 3: Store the Caller Function Name in a Variable

Instead of printing the caller function name directly, we might want to store it in a variable for further processing.

```python
def function1():
    function2()
    
def function2():

    caller_function_name = inspect.stack()[1][3]
    
    return caller_function_name
    
caller_name = function2()
print(caller_name)
```

## Conclusion

In this article, we learned how to retrieve the caller function name inside another function in Python using the inspect module. We also saw how to store the caller function name in a variable. This can be useful in scenarios where we want to perform some actions based on the caller function.
