---
title: What is the process for deleting several indices altogether from a list simultaneously?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use a list comprehension to create a new list with only the elements that do not correspond to the desired indexes.
---

**Contents**

[TOC]

## Introduction

In Python, we can remove multiple indexes from a list at the same time in different ways. In this tutorial, we will discuss a few methods for removing multiple indexes from a list.


## Using List Comprehension

One way to remove multiple indexes from a list is to use list comprehension. We can create a new list by iterating over the original list and excluding the desired indexes. Here's an example:

```python
nums = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# removing indexes 2, 5, and 9
new_nums = [nums[i] for i in range(len(nums)) if i not in [2, 5, 9]]

print(new_nums)
# Output: [0, 1, 3, 4, 6, 7, 8]
```

In this example, we use a list comprehension to iterate over the original list `nums`. We include all elements in `nums` except the ones at indexes 2, 5, and 9. The resulting list `new_nums` contains only the remaining elements.


## Using Slice Assignment

Another way to remove multiple indexes from a list is to use slice assignment. We can slice the original list and assign the sliced value to the same list. Here's an example:

```python
nums = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# removing indexes 2, 5, and 9
del nums[9]
del nums[5]
del nums[2]

print(nums)
# Output: [0, 1, 3, 4, 6, 7, 8]
```

In this example, we use slice assignment to remove the elements at indexes 2, 5, and 9 from the original list `nums`. We simply delete the elements at these indexes using the `del` keyword.


## Using List Comprehension with Enumerate

Another way to remove multiple indexes from a list is to use list comprehension along with `enumerate()`. We can iterate over the original list along with their indexes using `enumerate()`, and exclude the desired indexes. Here's an example:

```python
nums = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# removing indexes 2, 5, and 9
new_nums = [nums[i] for i, num in enumerate(nums) if i not in [2, 5, 9]]

print(new_nums)
# Output: [0, 1, 3, 4, 6, 7, 8]
```

In this example, we use list comprehension along with `enumerate()` to iterate over the original list `nums` along with their indexes. We include all elements in `nums` except the ones at indexes 2, 5, and 9. The resulting list `new_nums` contains only the remaining elements.


## Conclusion

In this tutorial, we discussed a few methods for removing multiple indexes from a list in Python. We can use list comprehension, slice assignment, or list comprehension with `enumerate()`, depending on our use case. These methods are straightforward and efficient for removing multiple list elements.
