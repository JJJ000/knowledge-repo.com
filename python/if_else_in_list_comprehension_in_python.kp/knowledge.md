---
title: A list comprehension with an 'if else' statement could look like [x if condition else y for x in iterable]
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: It is not possible to use an if-else statement in a list comprehension in Python.
---

**Contents**

[TOC]

**Section 1: Syntax**

The syntax for an if-else statement in a list comprehension is as follows: 

`[<expression> if <condition> else <expression> for <variable> in <iterable>]`

**Section 2: Example**

For example, the following list comprehension returns a list of squared numbers for all numbers less than 10 and a list of -1 for all other numbers:

`[x**2 if x < 10 else -1 for x in range(20)]`

**Section 3: Output**

The output of the above list comprehension is: 

`[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, -1, -1, -1, -1, -1, -1, -1, -1, -1, -1]`

**Section 4: Explanation**

The list comprehension iterates through the range 0 to 19 (`range(20)`) and checks if the current number is less than 10 (`x < 10`). If the condition is true, it squares the number (`x**2`) and adds it to the list. If the condition is false, it adds -1 to the list.
