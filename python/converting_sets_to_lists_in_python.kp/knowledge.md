---
title: What is the process of converting a set to a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the list() function to convert a set to a list in Python.
---

**Contents**

[TOC]

## Section 1: Understanding sets and lists in Python

Before we can convert a set to a list, it's important to understand what sets and lists are in Python.

- A **set** is a collection of unique elements, where order doesn't matter. Sets are enclosed in curly braces `{}` or can be created using the `set()` function.

- A **list** is a collection of ordered elements, where each element has a specific index number starting from 0. Lists are enclosed in square brackets `[]` or can be created using the `list()` function.

## Section 2: Converting a set to a list using typecasting

One way to convert a set to a list is to use typecasting. Typecasting is the process of converting one data type to another. We can use the `list()` function to typecast a set to a list.

Here's an example:

```python
# set of fruits
fruits_set = {'apple', 'banana', 'orange', 'grape'}

# convert set to list
fruits_list = list(fruits_set)

print(fruits_list)
```

Output:
```
['banana', 'grape', 'orange', 'apple']
```
We first created a set of fruits and assigned it to the variable `fruits_set`. Then, we used the `list()` function to convert this set to a list and assigned it to the variable `fruits_list`. We printed the resulting list using `print()`.

## Section 3: Sorting a list converted from a set

Since a set does not preserve the order of its elements, it's important to note that the resulting list from the previous step will not be sorted. However, we can sort the list using the `sorted()` function.

Here's an example:

```python
# set of fruits
fruits_set = {'apple', 'banana', 'orange', 'grape'}

# convert set to list
fruits_list = list(fruits_set)

# sort the list
sorted_fruits_list = sorted(fruits_list)

print(sorted_fruits_list)
```

Output:
```
['apple', 'banana', 'grape', 'orange']
```
We first created a set of fruits and assigned it to the variable `fruits_set`. Then, we used the `list()` function to convert this set to a list and assigned it to the variable `fruits_list`. We sorted the resulting list using the `sorted()` function and assigned it to the variable `sorted_fruits_list`. We printed the sorted list using `print()`.

## Section 4: Alternative method for sorting a list

An alternative method for sorting a list is to use the `sort()` method. This method sorts the list in place, meaning that it modifies the original list.

Here's an example:

```python
# set of fruits
fruits_set = {'apple', 'banana', 'orange', 'grape'}

# convert set to list
fruits_list = list(fruits_set)

# sort the list using the sort() method
fruits_list.sort()

print(fruits_list)
```

Output:
```
['apple', 'banana', 'grape', 'orange']
```
We first created a set of fruits and assigned it to the variable `fruits_set`. Then, we used the `list()` function to convert this set to a list and assigned it to the variable `fruits_list`. We sorted the resulting list using the `sort()` method. We printed the sorted list using `print()`. Note that the original list has been modified and is now sorted.
