---
title: What is the accurate way to write the syntax for 'else if'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The correct syntax for `else if` in Python is `elif`.
---

**Contents**

[TOC]

## Introduction
Conditional statements in programming languages allow us to make decisions and execute specific pieces of code based on whether a certain condition(s) is true or false. In Python, we have different ways of implementing conditional statements. We have the `if` statement, `if...else` statement, and the `if...elif...else` statement, which we will cover in this article.

## If Statement
The `if` statement is the most basic conditional statement in Python. It allows us to execute a block of code if a certain condition is true. Here's the syntax for an `if` statement:

``` python
if condition:
    # execute code here
```

Where `condition` is any expression that evaluates to either `True` or `False`. If the condition is true, the code block indented under it is executed. If the condition is false, nothing is executed. 

Here's an example:

``` python
x = 5
if x > 2:
    print("x is greater than 2")
```

In this case, the condition `x > 2` is true, and the code block indented under it is executed. The output of this code would be:

```
x is greater than 2
```

## If...Else Statement
The `if...else` statement allows us to execute different code blocks depending on whether a condition is true or false. Here's the syntax for an `if...else` statement:

``` python
if condition:
    # execute code block if condition is true
else:
    # execute code block if condition is false
```

Here's an example:

``` python
x = 10
if x > 15:
    print("x is greater than 15")
else:
    print("x is less than or equal to 15")
```

In this case, the condition `x > 15` is false, so the code block indented under `else` is executed. The output of this code would be:

```
x is less than or equal to 15
```

## If...Elif...Else Statement
The `if...elif...else` statement allows us to execute different code blocks depending on multiple conditions. Here's the syntax for an `if...elif...else` statement:

``` python
if condition1:
    # execute code block if condition1 is true
elif condition2:
    # execute code block if condition2 is true and condition1 is false
else:
    # execute code block if both condition1 and condition2 are false
```

Here's an example:

``` python
x = 20
if x > 30:
    print("x is greater than 30")
elif x > 15:
    print("x is greater than 15 but less than or equal to 30")
else:
    print("x is less than or equal to 15")
```

In this case, `x > 30` is false, so the code block under `if` is not executed. `x > 15` is true, so the code block under `elif` is executed. The output of this code would be:

```
x is greater than 15 but less than or equal to 30
```

If both `x > 30` and `x > 15` were false, the code block under `else` would be executed.
