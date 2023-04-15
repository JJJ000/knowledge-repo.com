---
title: What is the process for verifying whether all items in a list adhere to a certain criterion?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the all() function with a list comprehension or generator expression to check if all elements of a list match a condition in Python.
---

**Contents**

[TOC]

## Introduction

In Python, we often come across situations where we need to check if all elements of a list match a certain condition. This can be done in various ways using different methods provided by Python. In this article, we will look at some of the ways to achieve this.

## List comprehension

List comprehension is a very powerful and concise way of creating a new list from an existing list based on certain conditions. We can use this technique to check if all elements of a list match a specific condition.

Here's how we can use list comprehension to check if all elements of a list are even:

```python
my_list = [2, 4, 6, 8, 10]
all_even = all(x % 2 == 0 for x in my_list)
```

In this example, we first create a new list using list comprehension that checks if each element of `my_list` is even or not. We then pass this list to the `all` function which returns `True` if all elements of the list are `True`, otherwise it returns `False`.

## Using map and all functions

Another way to check if all elements of a list match a condition is by using the `map` function together with the `all` function. The `map` function allows us to apply a function to each element of a list and returns the result as a new list.

Here's an example of how we can use `map` and `all` functions to check if all elements of a list are even:

```python
my_list = [2, 4, 6, 8, 10]
all_even = all(map(lambda x: x % 2 == 0, my_list))
```

In this example, we use the `lambda` function to create a function that checks if a given number is even or not. We then use `map` function to apply this function to each element of `my_list` and create a new list of boolean values. Finally, we pass this new list to the `all` function to check if all elements are `True`.

## Using the filter and len functions

We can also use the `filter` function to filter out elements of a list that don't match a certain condition, and then use the `len` function to check if the length of the resulting list is equal to the original list.

Here's an example of how we can use `filter` and `len` functions to check if all elements of a list are even:

```python
my_list = [2, 4, 6, 8, 10]
all_even = len(filter(lambda x: x % 2 == 0, my_list)) == len(my_list)
```

In this example, we use the `lambda` function to create a function that checks if a given number is even or not. We then use `filter` function to filter out elements of `my_list` that don't match this condition, and we get a new list of even numbers. Finally, we check if the length of this new list is equal to the length of the original list to test if all elements are even.

## Conclusion

In this article, we have seen three different ways of checking if all elements of a list match a certain condition. We discussed using list comprehension, map and all functions, and filter and len functions. Depending on the scenario, one method may be more appropriate over the others. It's important to choose the one that fits the requirement and is most efficient.
