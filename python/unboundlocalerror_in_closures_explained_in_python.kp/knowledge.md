---
title: What is the reason behind the occurrence of this unboundlocalerror (closure)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The UnboundLocalError occurs in Python when trying to access a local variable before it is assigned a value within a function or closure.
---

**Contents**

[TOC]

## Overview

The UnboundLocalError is a common error message that occurs in Python when trying to reference a local variable before it is assigned a value. It is usually caused by a scoping issue - when the Python interpreter is unable to locate a variable within the scope of the function.

## Scopes in Python

Scopes in Python define the accessibility of a variable. There are three main types of scopes in Python:
 
- Local scope: Variables defined within a function are local to that function and cannot be accessed outside of it.
- Enclosing scope: Variables defined in an outer function can be accessed by inner functions within that function.
- Global scope: Variables defined outside of any function can be accessed anywhere in the program.

## Closure in Python

Closure in Python refers to the ability of a function to remember and access the values of non-local variables even when the outer function has returned. 

This is possible because Python supports nested functions which allows a function to be defined inside another function. The inner function can then take advantage of the variables and names defined in the outer function, even after the outer function has completed execution.

## UnboundLocalError in Closures

The UnboundLocalError can occur in closures when a variable is referenced in a nested function, but not assigned a value in the local scope of that function. 

For example, consider the following code:

```
def outer_function():
    x = 5

    def inner_function():
        print(x)
        x = 10

    inner_function()

outer_function()
```

In this code, the variable `x` is defined in the outer function and is also accessed in the inner function. However, since `x` is assigned a value in the inner function after it is referenced, the UnboundLocalError will be raised.

To avoid this error, we can use the `nonlocal` keyword to indicate that `x` is a non-local variable and should be accessed from the outer function. The modified code would look like this:

```
def outer_function():
    x = 5

    def inner_function():
        nonlocal x
        print(x)
        x = 10

    inner_function()

outer_function()
```

In this code, the `nonlocal` keyword tells Python that `x` is not a local variable, but is defined in the outer scope. 

With this modification, the UnboundLocalError is resolved and the code executes without error.
