---
title: What is the syntax for the sorted function when using lambda as the key?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Syntax `sorted()` function in Python with `key=lambda` parameter allows the user to sort a collection based on a custom function, defined with lambda.
---

**Contents**

[TOC]

Section 1: Introduction
The sorted function in python returns a sorted list of elements from the given iterable, with the option to specify a custom key function that determines the sorting order. The key function should take in only one argument and should return a value that will be used to compare the elements in the iterable.

Section 2: The lambda function
The lambda function is an anonymous function that can be defined on the fly. It takes in any number of arguments and returns a value, just like a regular function. However, it doesn't have a function name, so it can only be called through a variable that points to it. In this case, we define the key function for the sorted function with a lambda function, which is a shortcut way to define a small function without explicitly naming it.

Section 3: The key parameter
The key parameter in the sorted function is used to specify a function to customize the sorting order of the elements in the iterable. When we use the lambda function to define the key function, we are essentially saying that we want to sort the elements based on the output of the lambda function for each element in the iterable. We can specify any type of comparison logic inside the lambda function, including string comparisons, numerical comparisons, or a combination of both.

Section 4: Examples
Here's an example of using the sorted function with the lambda function as the key parameter:
```
>>> my_list = ['apple', 'banana', 'orange', 'pear']
>>> sorted_list = sorted(my_list, key=lambda x: len(x))
>>> print(sorted_list)
['pear', 'apple', 'banana', 'orange']
```
In this example, we're sorting the list of fruits based on the length of their names. The lambda function takes in each fruit name as an argument and returns the length of the name, which is then used to compare the elements and sort them accordingly.
