---
title: What is the method for verifying if a smaller dictionary is included in a larger dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the set operator `<=` to check if all items in the smaller dictionary are also in the larger dictionary.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, we can easily check if one dictionary is a subset of another larger dictionary using the `items()` method and the `issubset()` method. In this tutorial, we will learn how to do this in detail.

## Section 2: Checking if a Dictionary is a Subset of Another Dictionary
To check if one dictionary is a subset of another larger dictionary in Python, we can use the `items()` method to get the key-value pairs of both dictionaries as sets, and then use the `issubset()` method to check if the first set is a subset of the second set. Here's the code:

```
def is_subset(dict1, dict2):
    return set(dict1.items()).issubset(set(dict2.items()))
```

In this code, the `is_subset()` function takes two dictionaries as arguments and returns `True` if the first dictionary is a subset of the second dictionary, and `False` otherwise. The `set()` method is used to convert the key-value pairs of both dictionaries into sets. The `items()` method returns a list of tuples containing the key-value pairs of each dictionary, which is then converted into a set.


## Section 3: Example
Let's see an example of how to use the function:

```
dict1 = {'a': 1, 'b': 2}
dict2 = {'a': 1, 'b': 2, 'c': 3, 'd': 4}

print(is_subset(dict1, dict2))     # Output: True
```

In this example, the `dict1` dictionary is a subset of the `dict2` dictionary because all the key-value pairs of `dict1` are present in `dict2`.

## Section 4: Conclusion
In this tutorial, we learned how to check if one dictionary is a subset of another larger dictionary in Python. We saw that we can use the `items()` method and the `issubset()` method to easily perform this operation. We also saw an example of how to use this function in Python.
