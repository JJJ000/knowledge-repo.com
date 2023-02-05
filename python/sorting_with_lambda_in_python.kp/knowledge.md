---
title: Using lambda to sort data in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the sorted() function and pass in a lambda expression as the key argument to sort with lambda in Python.
---

**Contents**

[TOC]

1. Introduction
--------------------
Python's lambda functions allow us to create anonymous functions, which can be used to sort data in a variety of ways. Lambda functions are a powerful tool for manipulating data, and can be used to sort data in a number of different ways. In this article, we will discuss how to use lambda functions to sort data in Python.

2. Syntax
--------------------
The basic syntax for a lambda function is as follows:

`lambda argument_list : expression`

The argument_list is a list of arguments that are passed to the lambda function, and the expression is the code that is executed when the lambda function is called.

3. Examples
--------------------
To demonstrate how to use lambda functions to sort data in Python, we will use a list of numbers:

`nums = [3, 5, 2, 1, 4]`

We can use a lambda function to sort this list in ascending order:

`sorted_nums = sorted(nums, key=lambda x: x)`

This will give us a sorted list:

`[1, 2, 3, 4, 5]`

We can also use a lambda function to sort this list in descending order:

`sorted_nums = sorted(nums, key=lambda x: -x)`

This will give us a sorted list:

`[5, 4, 3, 2, 1]`

4. Conclusion
--------------------
In this article, we discussed how to use lambda functions to sort data in Python. Lambda functions are a powerful tool for manipulating data, and can be used to sort data in a number of different ways. We demonstrated how to use lambda functions to sort a list of numbers in both ascending and descending order.
