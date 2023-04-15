---
title: Reword 'if not' syntax in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The `if not` syntax in Python checks if a condition is false.
---

**Contents**

[TOC]

# Introduction

Python has a variety of conditional statements that are used to make decisions in programming. One such statement is the "if not" statement, which allows you to check whether a condition is not true.

# Basic Syntax

The basic syntax of the "if not" statement is as follows:

```python
if not condition:
    # do something if condition is not true
```

In this code, the "condition" is the expression that you want to check. If the condition is not true, the code block beneath it will be executed. If the condition is true, the code block will be skipped.

# Using "if not" with Logical Operators

The "not" keyword can also be used in combination with other logical operators to create more complex conditional statements. For example:

```python
if not (x == 1 and y == 2):
    # do something if x is not 1 OR y is not 2
```

Here, the "not" keyword is used in combination with the "and" operator to check whether both x is not equal to 1 AND y is not equal to 2.

# Using "if not" with Boolean Values

The "not" keyword can also be used with boolean values to make decisions based on whether a value is False. For example:

```python
x = False

if not x:
    print("x is not True")
```

In this code, the "not" keyword is used to check whether "x" is not true. Since "x" is False, the code block will be executed.

# Conclusion

The "if not" statement allows you to test whether a condition is not true. This can be useful in a variety of situations, from simple boolean checks to more complex conditional statements. Knowing how to use this statement effectively is an important part of writing robust and reliable Python code.
