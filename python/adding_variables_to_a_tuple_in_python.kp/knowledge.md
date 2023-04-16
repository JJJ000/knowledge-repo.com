---
title: Include variables in tuple
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Tuples are immutable, so variables cannot be added to them directly.
---

**Contents**

[TOC]

### Adding Elements to a Tuple

Tuples are immutable, so you cannot add elements to a tuple. You can create a new tuple that contains the elements of the original tuple and the new elements.

### Creating a New Tuple

To create a new tuple that contains the elements of the original tuple and the new elements, you can use the `+` operator. For example, if you have a tuple `tup1 = (1, 2, 3)` and you want to add the element `4`, you can use the `+` operator to create a new tuple `tup2 = tup1 + (4,)`.

### Concatenating Tuples

You can also use the `+` operator to concatenate two tuples. For example, if you have two tuples `tup1 = (1, 2, 3)` and `tup2 = (4, 5, 6)`, you can use the `+` operator to create a new tuple `tup3 = tup1 + tup2`.

### Using the `tuple()` Function

You can also use the `tuple()` function to add elements to a tuple. The `tuple()` function takes a sequence as an argument and returns a tuple. For example, if you have a list `lst = [1, 2, 3]` and you want to add the element `4`, you can use the `tuple()` function to create a new tuple `tup = tuple(lst + [4])`.
