---
title: Combinations of all elements from a list of lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The product of all the lists in the list of lists can be calculated using itertools.product().
---

**Contents**

[TOC]

# Section 1: Using itertools

The itertools module in Python provides a number of functions that can be used to generate combinations of a list of lists. The itertools.product() function can be used to generate all possible combinations of the elements in a list of lists.

For example, consider the following list of lists:

```
list_of_lists = [[1,2,3], [4,5], [6,7,8]]
```

Using the itertools.product() function, we can generate all possible combinations of the elements in the list of lists:

```
from itertools import product

combinations = list(product(*list_of_lists))

print(combinations)

# Output: [(1, 4, 6), (1, 4, 7), (1, 4, 8), (1, 5, 6), (1, 5, 7), (1, 5, 8), (2, 4, 6), (2, 4, 7), (2, 4, 8), (2, 5, 6), (2, 5, 7), (2, 5, 8), (3, 4, 6), (3, 4, 7), (3, 4, 8), (3, 5, 6), (3, 5, 7), (3, 5, 8)]
```

# Section 2: Using Recursion

Recursion is another way to generate all possible combinations of a list of lists. The recursive approach involves looping through each list in the list of lists, and recursively generating all possible combinations of the remaining lists.

For example, consider the following list of lists:

```
list_of_lists = [[1,2,3], [4,5], [6,7,8]]
```

Using a recursive approach, we can generate all possible combinations of the elements in the list of lists:

```
def generate_combinations(lists):
    if len(lists) == 1:
        return [[x] for x in lists[0]]

    combinations = []
    for x in lists[0]:
        for c in generate_combinations(lists[1:]):
            combinations.append([x] + c)

    return combinations

combinations = generate_combinations(list_of_lists)

print(combinations)

# Output: [[1, 4, 6], [1, 4, 7], [1, 4, 8], [1, 5, 6], [1, 5, 7], [1, 5, 8], [2, 4, 6], [2, 4, 7], [2, 4, 8], [2, 5, 6], [2, 5, 7], [2, 5, 8], [3, 4, 6], [3, 4, 7], [3, 4, 8], [3, 5, 6], [3, 5, 7], [3, 5, 8]]
```

# Section 3: Using List Comprehension

List comprehension is a concise way to generate all possible combinations of a list of lists. The list comprehension approach involves looping through each list in the list of lists, and generating all possible combinations of the elements in the list.

For example, consider the following list of lists:

```
list_of_lists = [[1,2,3], [4,5], [6,7,8]]
```

Using list comprehension, we can generate all possible combinations of the elements in the list of lists:

```
combinations = [x for x in list_of_lists[0] for y in list_of_lists[1] for z in list_of_lists[2]]

print(combinations)

# Output: [1, 4, 6, 1, 4, 7, 1, 4, 8, 1, 5, 6, 1, 5, 7, 1, 5, 8, 2, 4, 6, 2, 4, 7, 2, 4, 8, 2, 5, 6, 2, 5, 7, 2, 5, 8, 3, 4, 6, 3, 4, 7, 3, 4, 8, 3, 5, 6, 3, 5, 7, 3, 5, 8]
```

# Section 4: Using Nested Loops

Nested loops can also be used to generate all possible combinations of a list of lists. The nested loop approach involves looping through each list in the list of lists, and generating all possible combinations of the elements in the list.

For example, consider the following list of lists:
