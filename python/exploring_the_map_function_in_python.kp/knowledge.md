---
title: Grasping the purpose of the map function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The map function in Python applies a given function to every item in an iterable object and returns a list of the results.
---

**Contents**

[TOC]

**Section 1: Overview**

The map() function in Python is a built-in function that applies a function to every item of an iterable (such as a list, tuple, set, or dictionary) and returns a list of the results. It takes two parameters: a function and an iterable. The function is applied to each item of the iterable, and the result is a new list containing all the modified items.

**Section 2: Syntax**

The syntax of the map() function is as follows:

```
map(function, iterable)
```

Where function is the function to be applied to each item of the iterable, and iterable is the iterable containing the items to be modified.

**Section 3: Example**

For example, if we wanted to multiply each item in a list by 2, we could use the map() function as follows:

```
list_a = [1, 2, 3, 4]

list_b = list(map(lambda x:x*2, list_a))

print(list_b)
```

This would output:

```
[2, 4, 6, 8]
```

**Section 4: Limitations**

The map() function can only be used with functions that take one argument. If the function takes multiple arguments, it must be wrapped in a lambda expression. Additionally, the map() function returns a map object, which must be converted to a list or other iterable before it can be used.
