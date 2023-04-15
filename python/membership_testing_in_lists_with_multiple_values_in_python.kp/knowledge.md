---
title: What is the way to determine if multiple values are part of a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `in` operator followed by a list of values to test for membership in a given list.
---

**Contents**

[TOC]

## Introduction
In Python, we often need to check if multiple values exist in a list or not. There are several ways to do this. In this article, we will explore some of the most common methods to test the membership of multiple values in a list in Python.

## Using Set Intersection
One way to test for the membership of multiple values in a list is to convert the list to a set and then use the set intersection method to check if the values are present in the set. Here is an example:

```
lst = [1, 2, 3, 4, 5]
values = [2, 4]

if set(lst).intersection(values):
    print("All values are present in the list")
else:
    print("Some values are missing")
```

In this example, we first create a list `lst` and a list of `values` we want to check for. We then convert `lst` to a set using the `set()` function and find the intersection of this set with the `values` list using the `intersection()` method. If the result is not an empty set, it means that all of the values are present in `lst`.

## Using the "all" Function
Another way to check for the membership of multiple values in a list is to use the built-in `all()` function. This function takes an iterable and returns `True` if all elements of the iterable are True. Here is an example:

```
lst = [1, 2, 3, 4, 5]
values = [2, 4]

if all(val in lst for val in values):
    print("All values are present in the list")
else:
    print("Some values are missing")
```

In this example, we use a list comprehension to iterate over each value in `values` and check if it is in `lst`. The resulting list of Boolean values is passed to the `all()` function, which returns `True` if all values are `True`.

## Using the "in" Keyword with Logical Operators
We can also use the `in` keyword with logical operators to check for the membership of multiple values in a list. Here is an example:

```
lst = [1, 2, 3, 4, 5]
values = [2, 4]

if all(val in lst for val in values):
    print("All values are present in the list")
else:
    print("Some values are missing")
```

In this example, we combine multiple `in` operators with the logical `and` operator to check if all values are present in `lst`. This code is equivalent to the previous example using the `all()` function but may be more verbose.

## Using the Counter Object
Finally, we can use the `Counter` object from the built-in `collections` module to count the occurrences of each value in both the list and the values we want to check for. Here is an example:

```
from collections import Counter

lst = [1, 2, 3, 4, 5]
values = [2, 4]

lst_counts = Counter(lst)
values_counts = Counter(values)

if all(lst_counts[val] >= values_counts[val] for val in values):
    print("All values are present in the list")
else:
    print("Some values are missing")
```

In this example, we create two `Counter` objects, one for `lst` and one for `values`. We then use a list comprehension to iterate over each value in `values` and check if its count in `lst` is greater than or equal to its count in `values`. If this is true for all values, it means that all values are present in `lst`.
