---
title: In accordance with the length of a shorter list, what methods can I use to correspond permutations of a lengthy list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use itertools.permutations to generate permutations of the long list, then iterate through the permutations and match each one to a slice of the shorter list by using slicing and comparing elements.
---

**Contents**

[TOC]

## Section 1: Understanding the problem

Before solving the problem, we need to understand the problem requirements and constraints. Based on the problem statement, we need to match up permutations of a long list with a shorter list according to the length of the shorter list. This means that we need to generate all possible permutations of the long list and then match them with the shorter list.

For example, suppose we have a long list with 6 elements and a short list with 3 elements. We need to generate all possible permutations of the long list and then match each permutation with the short list. If there are 4 permutations that match the short list, we need to return those 4 permutations.

To implement this, we can use Python's `itertools` module to generate permutations and then match these permutations with the shorter list.

## Section 2: Generating permutations

To generate all possible permutations of the long list, we can use the `permutations` function from Python's `itertools` module. This function takes an iterable (the long list in our case) and a length (the length of the shorter list) and returns an iterator over all possible permutations of that iterable with the given length.

Here's an example code snippet that generates all possible permutations of a long list with 6 elements and a short list with 3 elements:

```python
from itertools import permutations

long_list = [1, 2, 3, 4, 5, 6]
short_list = [2, 3, 6]
short_list_len = len(short_list)

permutations_iter = permutations(long_list, short_list_len)

for permutation in permutations_iter:
    # Match permutation with short_list
```

## Section 3: Matching permutations with the short list

Once we have generated all possible permutations of the long list, we need to match each permutation with the short list. To do this, we can simply iterate over each permutation and check if it matches the short list.

Here's an implementation of the matching logic:

```python
from itertools import permutations

long_list = [1, 2, 3, 4, 5, 6]
short_list = [2, 3, 6]
short_list_len = len(short_list)

permutations_iter = permutations(long_list, short_list_len)

matching_permutations = []

for permutation in permutations_iter:
    if list(permutation) == short_list:
        matching_permutations.append(permutation)

print(matching_permutations)
```

In this implementation, we are converting the permutation (which is an iterator) to a list so that we can compare it with the short list using the `==` operator. If a permutation matches the short list, we append it to the `matching_permutations` list.

## Section 4: Putting it all together

Now that we have the logic to generate permutations and match them with the short list, we can put everything together into a single function. Here's the final implementation:

```python
from itertools import permutations

def match_permutations(long_list, short_list):
    short_list_len = len(short_list)

    permutations_iter = permutations(long_list, short_list_len)

    matching_permutations = []

    for permutation in permutations_iter:
        if list(permutation) == short_list:
            matching_permutations.append(permutation)

    return matching_permutations
```

This function takes a long list and a short list as input and returns a list of all permutations that match the short list. To use this function, simply call it with the long and short lists:

```python
long_list = [1, 2, 3, 4, 5, 6]
short_list = [2, 3, 6]

matching_permutations = match_permutations(long_list, short_list)

print(matching_permutations)
```
