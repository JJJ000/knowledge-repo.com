---
title: Locate the first element in the sequence that meets the criteria
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The first sequence item that matches a criterion can be found using the index() method, which returns the index of the first item that matches the specified criterion.
---

**Contents**

[TOC]

# Using the `filter()` Function

The `filter()` function is a useful tool for finding the first sequence item that matches a criterion. This function takes two arguments: a function and an iterable. The function should take one argument and return a Boolean value (`True` or `False`). The iterable can be any type of sequence, such as a list, tuple, or string.

The `filter()` function will return a filter object containing only the items from the sequence that match the criterion. To get the first item from the filter object, we can use the `next()` function.

# Example

For example, if we have a list of numbers and we want to find the first number that is divisible by 3, we can use the `filter()` and `next()` functions:

```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Create a function that checks if a number is divisible by 3
def is_divisible_by_3(num):
    return num % 3 == 0

# Use filter to create a filter object containing only the numbers divisible by 3
filtered_numbers = filter(is_divisible_by_3, numbers)

# Use next to get the first item from the filter object
first_number = next(filtered_numbers)

print(first_number) # 3
```

# Conclusion

The `filter()` and `next()` functions can be used together to find the first sequence item that matches a criterion. This can be a useful tool for quickly finding the first item in a sequence that meets a certain condition.
