---
title: A list comprehension with an if/else statement can be written as [x if condition else y for x in iterable]
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, it is not possible to use if/else in a list comprehension in Python.
---

**Contents**

[TOC]

**Using an if/else Statement**

The if/else statement can be used in a list comprehension to check for a condition and return one result if the condition is true and another result if the condition is false. The syntax is as follows:

```
[expression if condition else other_expression for item in list]
```

**Example**

Here is an example of a list comprehension that uses an if/else statement to check for even numbers in a list and return the number multiplied by two if it is even, or the number divided by two if it is odd:

```
numbers = [1, 2, 3, 4, 5]
result = [num * 2 if num % 2 == 0 else num / 2 for num in numbers]

# result = [0.5, 4, 1.5, 8, 2.5]
```

**Using Multiple if/else Statements**

The if/else statement can also be used in a list comprehension to check for multiple conditions and return different results depending on which condition is true. The syntax is as follows:

```
[expression_1 if condition_1 else expression_2 if condition_2 else expression_3 for item in list]
```

**Example**

Here is an example of a list comprehension that uses multiple if/else statements to check for numbers in a list and return the number multiplied by three if it is divisible by three, the number multiplied by two if it is divisible by two, or the number divided by two if it is not divisible by either two or three:

```
numbers = [1, 2, 3, 4, 5, 6]
result = [num * 3 if num % 3 == 0 else num * 2 if num % 2 == 0 else num / 2 for num in numbers]

# result = [0.5, 4, 9, 8, 2.5, 12]
```
