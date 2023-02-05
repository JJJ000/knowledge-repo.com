---
title: A unboundlocalerror has occurred in Python 3, indicating that a local variable has been referenced before it has been assigned a value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A UnboundLocalError occurs when a local variable is referenced before it has been assigned a value.
---

**Contents**

[TOC]

# Overview
An UnboundLocalError occurs when a local variable is referenced before it is assigned a value. This error is specific to Python 3 and is not present in Python 2.

# Causes
This error is caused when a variable is used before it is assigned a value. This can happen in a few different ways.

1. When a variable is used before it is declared. 
2. When a variable is used in a nested scope before it is assigned in the outer scope. 
3. When a variable is used before it is assigned in a loop.

# Examples
1. Using a variable before it is declared:
```
x = 10
print(y)
y = 20
```
This will result in an UnboundLocalError because the variable y is used before it is declared.

2. Using a variable in a nested scope before it is assigned in the outer scope:
```
x = 10
def my_function():
    print(x)
    x = 20

my_function()
```
This will result in an UnboundLocalError because the variable x is used in the nested scope before it is assigned in the outer scope.

3. Using a variable before it is assigned in a loop:
```
for x in range(10):
    print(x)
    x = 20
```
This will result in an UnboundLocalError because the variable x is used before it is assigned in the loop.

# Solutions
1. Declare the variable before it is used:
```
x = 10
y = 20
print(y)
```

2. Assign the variable in the outer scope before it is used in the nested scope:
```
x = 10
def my_function():
    print(x)
    x = 20

my_function()
```

3. Assign the variable in the loop before it is used:
```
for x in range(10):
    x = 20
    print(x)
```
