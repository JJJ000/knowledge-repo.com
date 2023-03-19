---
title: Does Python 3 have a 'foreach' function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, Python 3 has a built-in `foreach` function, which is called `for loop.`
---

**Contents**

[TOC]

What is a foreach function?
A foreach function is a loop construct used in programming languages to iterate over a collection of items and execute a block of code for each item.

Does Python 3 have a foreach function?
Python 3 does not have a traditional foreach function, but it does have several constructs that can be used to iterate over a collection of items:

1. for loop: The for loop in Python can be used to iterate over a range, a list, a tuple, a set, a dictionary, or any other iterable object. It follows the following syntax:

```python
for item in iterable:
    # execute block of code for each item
```

2. map() function: The map() function in Python applies a function to each item in an iterable object and returns a new iterable object with the results. It follows the following syntax:

```python
new_iterable = map(function, iterable)
```

3. list comprehension: List comprehensions in Python are a concise way of creating a new list by iterating over an existing iterable object and applying a condition. It follows the following syntax:

```python
new_list = [expression for item in iterable if condition]
```

4. generator expression: Generator expressions in Python are similar to list comprehensions but return a generator object instead of a list. It follows the following syntax:

```python
generator = (expression for item in iterable if condition)
```

Conclusion:
Python 3 does not have a traditional foreach function, but it has several constructs that can be used to achieve the same functionality. The most commonly used method is the for loop, which can iterate over any iterable object. The map() function, list comprehensions, and generator expressions are also useful constructs for iterating over iterable objects.
