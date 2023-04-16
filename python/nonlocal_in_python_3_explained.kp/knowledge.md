---
title: What is the purpose of the 'nonlocal' keyword in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Nonlocal allows a variable to be declared as nonlocal, which means it can be accessed and modified outside of the current scope.
---

**Contents**

[TOC]

# What is Nonlocal?
Nonlocal is a keyword in Python 3 that is used to declare variables that are not bound in the local scope. It allows for the modification of variables in an outer, but non-global, scope.

# When to Use Nonlocal
Nonlocal is used when a nested function needs to modify a variable in an outer, but non-global, scope. This allows the nested function to modify variables in the outer scope without having to pass them as arguments.

# Syntax
The syntax for using nonlocal is as follows:
```
nonlocal <variable_name>
```

# Example
The following example shows how nonlocal can be used to modify a variable in an outer scope:
```
x = 0

def outer():
    x = 1
    def inner():
        nonlocal x
        x = 2
    inner()
    print(x)

outer()
```
This code will print 2, because the nonlocal keyword allows the inner function to modify the variable x in the outer scope.
