---
title: What is the one-line way to condense if/else statements in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Using ternary operator (conditional expression) is a way to condense if/else into one line in Python.
---

**Contents**

[TOC]

There are a few ways to condense an if/else statement into one line in Python. Here are some options:

1. Ternary operators:
Ternary operators allow us to write if/else statements in a single line. Here's the general format:
`value_if_true if condition else value_if_false`
For example, consider the following if/else statement:
```
x = 5
if x > 0:
    y = 10
else:
    y = 20
```
We can condense this into a one-liner using a ternary operator like this:
`y = 10 if x > 0 else 20`
Notice that we put the value_if_true before the if keyword, and the value_if_false after the else keyword. 

2. Lambda functions:
Lambda functions are anonymous functions that can be defined in a single line. We can use a lambda function with a ternary operator to condense an if/else statement into a one-liner. Here's an example:
```
x = 5
y = (lambda a: 10 if a > 0 else 20)(x)
```
In this example, we define a lambda function that takes an argument a and returns 10 if a is greater than 0, and 20 otherwise. We immediately call this function with x as the argument, and assign the result to y.

3. Dictionary lookups:
If we have a series of if/else statements that assign different values to a variable based on a certain condition, we can use a dictionary to map the conditions to their corresponding values. Here's an example:
```
x = 5
y = {True: 10, False: 20}[x > 0]
```
In this example, we define a dictionary with two keys, True and False, mapped to 10 and 20 respectively. We then use the x > 0 expression as the key to look up the corresponding value from the dictionary and assign it to y.

4. Boolean operators:
If the if/else statement is simple enough, we can use boolean operators to condense it into a one-liner. For example:
```
x = 5
y = 10 if x > 0 else 20 if x <0 else 0
```
In this example, we're using nested if/else statements to check if x is greater than 0, less than 0, or equal to 0. We can simplify this by using the elif keyword and boolean operators like this:
`y = 10 if x > 0 else 20 if x < 0 else 0`
This code is equivalent to the previous if/else statement, but is condensed into a single line. However, this approach can quickly become unreadable if the if/else chain gets too long.
