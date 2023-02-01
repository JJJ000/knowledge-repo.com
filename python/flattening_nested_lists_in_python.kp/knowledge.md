---
title: Convert an irregularly nested list of lists into a single-level list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in function itertools.chain.from\_iterable to flatten an irregular (arbitrarily nested) list of lists in Python.
---

**Contents**

[TOC]

**Section 1: Understanding the Problem**

The problem is to flatten an irregular (arbitrarily nested) list of lists in Python. This means that the list can contain any number of elements and can be nested to any depth. The goal is to take this list and flatten it into a single-dimensional list.

**Section 2: Algorithm**

The algorithm for flattening an irregular list of lists can be broken down into the following steps:

1. Create an empty list to hold the flattened list.
2. Iterate over the list of lists.
3. If the element is a list, recursively call the flattening algorithm on it.
4. If the element is not a list, append it to the flattened list.
5. Return the flattened list.

**Section 3: Python Code**

The following Python code implements the algorithm described above:

```
def flatten_list(lst):
    flattened_list = []
    for element in lst:
        if isinstance(element, list):
            flattened_list.extend(flatten_list(element))
        else:
            flattened_list.append(element)
    return flattened_list
```

**Section 4: Example**

The following example demonstrates the use of the `flatten_list` function:

```
lst = [1, [2, 3], [4, [5, 6]]]
flattened_list = flatten_list(lst)
print(flattened_list)  # prints [1, 2, 3, 4, 5, 6]
```
