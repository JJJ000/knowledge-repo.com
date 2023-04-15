---
title: Retrieve the integer from a list that is nearest to a specified value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the min() function with key parameter set to lambda function that returns absolute difference between each number and the given value.
---

**Contents**

[TOC]

## Convert list of integers to absolute differences

One way to get the number closest to a given value from a list of integers is to first convert each integer into its absolute difference from the given value. This will give us a list of positive integers (or zero if the value is in the list). We can then find the minimum value in this list, which will correspond to the number closest to the given value.

Here's the code to do this:

```python
def closest_num(nums, target):
    abs_diffs = [abs(num - target) for num in nums]
    min_diff = min(abs_diffs)
    closest_num = nums[abs_diffs.index(min_diff)]
    return closest_num
```

This function takes two arguments: `nums`, which is the list of integers, and `target`, which is the value we want to find the closest number to. It first creates a new list `abs_diffs` by iterating over `nums` and computing the absolute difference between each number and `target`. Then it finds the minimum value in `abs_diffs` using the built-in `min` function. Finally, it returns the number in `nums` that corresponds to this minimum value, which is the closest number to `target`.


## Sort list by absolute differences

Another approach is to sort the list by the absolute differences between each number and the given value. This will allow us to easily identify the number closest to the target by simply looking at the first element of the sorted list.

Here is the code for this approach:

```python
def closest_num(nums, target):
    sorted_nums = sorted(nums, key=lambda x: abs(x - target))
    return sorted_nums[0]
```

This function takes the same arguments as before: `nums` and `target`. It first creates a new list `sorted_nums` by sorting `nums` according to the absolute differences between each number and `target`. To do this, we pass a lambda function to the `key` parameter of the `sorted` function that computes the absolute difference between each number and `target`. Finally, the function returns the first element of `sorted_nums`, which will be the number closest to `target`.


## Use the 'min()' function

Python has a built-in `min()` function that can also be used to find the closest number to a given value in a list of integers. We can pass a lambda function to `min()` that computes the absolute difference between each number and the target value. This will return the number in the list that has the smallest absolute difference from the target value.

Here is the code for this approach:

```python
def closest_num(nums, target):
    closest_num = min(nums, key=lambda x: abs(x - target))
    return closest_num
```

Again, this function takes two arguments: `nums` and `target`. It then uses the `min()` function to find the number in `nums` that has the smallest absolute difference from `target`. We pass a lambda function to `min()` that computes the absolute difference between each number and `target`. Finally, the function returns the closest number found. 


## Use NumPy

In case the list of numbers is quite large, NumPy can offer significant performance improvements. Here is the same example as before, but taking advantage of NumPy vectorization:

```python
import numpy as np

def closest_num(nums, target):
    abs_diffs = np.abs(np.array(nums) - target)
    min_diff = np.min(abs_diffs)
    closest_num = nums[np.where(abs_diffs == min_diff)[0][0]]
    return closest_num
```

This function is similar to the first example with `min()` instead of sorting. However, it firstly relies on NumPy to efficiently create a new numpy-array with the absolute differences, then obtain the value of the smallest absolute difference without iteration, and finally get the closest number without a loop.
