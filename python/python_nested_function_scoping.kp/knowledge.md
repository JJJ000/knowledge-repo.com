---
title: The scoping of variables in Python nested functions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Inner functions have access to variables in the outer function’s scope, but not vice versa.
---

**Contents**

[TOC]

# What are nested functions?

Nested functions are functions that are defined inside other functions. The inner function can access variables from the outer function, or even from the global scope. Nested functions can also be returned as values by the outer function, making them useful for creating closures.

# Variable scoping rules in nested functions

The scoping rules for variables in nested functions are based on the LEGB rule:

- Local: variables defined inside the function
- Enclosing: variables defined in the enclosing function
- Global: variables defined at the top level of the module
- Built-in: variables built into Python (e.g. print, len, etc.)

Variables are looked up in this order when they are referenced in the function. If a local variable with the same name as a variable in the enclosing or global scope is defined, the local variable takes precedence.

# Examples of nested function variable scoping

In this example, the inner function can access the variable x defined in the outer function:

```
def outer():
    x = 1
    def inner():
        print(x)
    inner()
```

When outer is called, it defines the variable x and then calls inner. When inner is called, it prints the value of x, which is 1.

In this example, the inner function defines a local variable with the same name as the variable in the outer function:

```
def outer():
    x = 1
    def inner():
        x = 2
        print(x)
    inner()
    print(x)
```

When outer is called, it defines the variable x and then calls inner. When inner is called, it defines a local variable also named x and sets it to 2. It then prints the value of the local variable, which is 2. When inner returns, outer prints the value of its own x variable, which is still 1.

In this example, the inner function modifies a mutable object defined in the outer function:

```
def outer():
    nums = [1, 2, 3]
    def inner():
        nums[0] = 4
        print(nums)
    inner()
    print(nums)
```

When outer is called, it defines the variable nums and sets it to a list of numbers. When inner is called, it modifies the first element of nums to be 4 and then prints the entire list. When inner returns, outer prints the modified version of nums. This shows that nested functions can modify objects defined in the outer function, but that re-assigning to a local variable shadows the outer variable.
