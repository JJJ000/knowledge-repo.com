---
title: What is the conventional approach in Python to retrieve a list of every nth element from a bigger list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use slicing with a step size of n.
---

**Contents**

[TOC]

Section 1: Problem statement
Given a larger list, we need to return a list containing every nth item from the original list.

Section 2: Solution
We can solve the problem using list slicing. List slicing is a powerful feature of python that allows us to extract a subset of a list. The syntax for list slicing is `list[start:end:step]`. Here, `start` is the starting index (inclusive), `end` is the ending index (exclusive), and `step` is the step size.

To extract every nth item from a list, we can set the `start` index to `n-1` and `step` to `n`. This will extract every `n`th item from the list, starting from the `n`th item.

Section 3: Python code
```python
def every_nth_item(lst, n):
    return lst[n-1::n]
```

Section 4: Explanation
The `every_nth_item` function takes two arguments: `lst`, which is the larger list from which we want to extract every nth item, and `n`, which is the value of `n`. The function returns a new list containing every nth item from the original list.

The list slicing syntax `lst[n-1::n]` specifies that we want to start at index `n-1` (since python lists are zero-indexed), take every `n`th item, and continue until the end of the list.

For example, if `lst` is `[1, 2, 3, 4, 5, 6, 7, 8, 9]`, and `n` is `3`, then `lst[n-1::n]` will evaluate to `[3, 6, 9]`, which is the list of every third item in the original list.

Thus, the `every_nth_item` function returns `[3, 6, 9]` for this example.
