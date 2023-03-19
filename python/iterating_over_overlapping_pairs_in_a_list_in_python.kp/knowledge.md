---
title: What is the process of iterating through pairs of values from a list which overlap each other (current and next)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the zip function with slicing to iterate over pairs of values in the list.
---

**Contents**

[TOC]

## 1. Approach

One approach to iterating over overlapping pairs in a list is to use a loop with a range that stops one index before the end of the list, and then access the current and next elements using their respective indices. 

## 2. Pseudo code

```python
for i in range(len(my_list) - 1):
    current_value = my_list[i]
    next_value = my_list[i+1]
    # Do something with the pair of values
```

## 3. Example implementation

Here is an example implementation using this approach:

```python
my_list = [1, 2, 3, 4, 5]

for i in range(len(my_list) - 1):
    current_value = my_list[i]
    next_value = my_list[i+1]
    print(current_value, next_value)
```

The output of this code will be:

```
1 2
2 3
3 4
4 5
```

## 4. Additional notes

It's worth noting that this approach only works for lists that have at least 2 elements. If a list has only one element or is empty, the loop will not execute at all. Also, if you only need to perform a specific operation on the pairs of values and don't need to store them, you can use the `zip()` function instead of a loop:

```python
for current_value, next_value in zip(my_list, my_list[1:]):
    # Do something with the pair of values
``` 

This has the advantage of being more concise and potentially faster for large lists, as it avoids having to access the list elements by indexing.
