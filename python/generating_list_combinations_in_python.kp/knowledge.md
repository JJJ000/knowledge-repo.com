---
title: What are all the possible combinations of elements in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use itertools.combinations() to generate all possible combinations of a list`s elements in Python.
---

**Contents**

[TOC]

# Using itertools

The `itertools` module in Python has a number of functions that can be used to generate iterators for efficient looping, including the `combinations()` function. This function can be used to get all possible combinations of a list’s elements.

## Syntax

The syntax for the `itertools.combinations()` function is as follows:

```
itertools.combinations(iterable, r)
```

Where `iterable` is the list of elements from which the combinations are to be generated, and `r` is the length of each combination.

## Example

Let's say we have a list of elements: `[1, 2, 3, 4]`. We can use the `itertools.combinations()` function to generate all possible combinations of length 2 from this list. The code for this is as follows:

```
from itertools import combinations

list_elements = [1, 2, 3, 4]
combinations_list = list(combinations(list_elements, 2))
print(combinations_list)
```

The output of this code will be:

```
[(1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4)]
```

# Using Recursion

Recursion is another method that can be used to generate all possible combinations of a list’s elements. This method involves defining a recursive function that takes a list of elements and an integer n as arguments. The function then generates all possible combinations of length n from the list.

## Syntax

The syntax for the recursive function is as follows:

```
def get_combinations(list_elements, n):
    if n == 0:
        return [[]]
    combinations_list = []
    for i in range(len(list_elements)):
        for next in get_combinations(list_elements[i+1:], n-1):
            combinations_list.append([list_elements[i]] + next)
    return combinations_list
```

Where `list_elements` is the list of elements from which the combinations are to be generated, and `n` is the length of each combination.

## Example

Let's say we have a list of elements: `[1, 2, 3, 4]`. We can use the recursive function to generate all possible combinations of length 2 from this list. The code for this is as follows:

```
def get_combinations(list_elements, n):
    if n == 0:
        return [[]]
    combinations_list = []
    for i in range(len(list_elements)):
        for next in get_combinations(list_elements[i+1:], n-1):
            combinations_list.append([list_elements[i]] + next)
    return combinations_list

list_elements = [1, 2, 3, 4]
combinations_list = get_combinations(list_elements, 2)
print(combinations_list)
```

The output of this code will be:

```
[[1, 2], [1, 3], [1, 4], [2, 3], [2, 4], [3, 4]]
```
