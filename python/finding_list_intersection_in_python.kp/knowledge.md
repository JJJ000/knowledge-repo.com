---
title: What is the intersection of two lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in `intersection` method of the set data type to find the intersection of two lists in Python.
---

**Contents**

[TOC]

### Using set()
The simplest way to find the intersection between two lists is by using the set() function. This function creates a set object, which is an unordered collection of unique elements.

To find the intersection of two lists, simply create two sets from the two lists and then use the `intersection()` method. This will return a set containing the elements that are common to both lists.

Example:

```
list_1 = [1, 2, 3, 4]
list_2 = [3, 4, 5, 6]

set_1 = set(list_1)
set_2 = set(list_2)

intersection = set_1.intersection(set_2)

print(intersection)
```

Output: `{3, 4}`

### Using list comprehensions
Another way to find the intersection of two lists is by using list comprehensions. This is a powerful way to create a new list from an existing list by applying a certain condition.

To find the intersection of two lists, create a new list that contains only the elements that are present in both lists.

Example:

```
list_1 = [1, 2, 3, 4]
list_2 = [3, 4, 5, 6]

intersection = [element for element in list_1 if element in list_2]

print(intersection)
```

Output: `[3, 4]`

### Using itertools
The `itertools` module in Python provides a number of functions that are useful when working with iterables. One of these functions is `intersect()`, which returns a generator object that contains the elements that are present in both lists.

Example:

```
list_1 = [1, 2, 3, 4]
list_2 = [3, 4, 5, 6]

import itertools

intersection = list(itertools.intersect(list_1, list_2))

print(intersection)
```

Output: `[3, 4]`
