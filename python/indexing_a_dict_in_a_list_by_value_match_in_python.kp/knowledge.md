---
title: Determine the position of a dictionary in a list by searching for a particular value in the dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a list comprehension and the enumerate function to loop through the list and find the index of the dictionary that matches the desired value.
---

**Contents**

[TOC]

## About the problem

In Python, we may have a list of dictionaries and we want to find the index of a dictionary in that list by matching the value of one of its keys. This is a common scenario when we need to retrieve a specific dictionary from a list based on a given condition.

## Solution approach 1: Using a for loop

One way to solve this issue is by iterating through the list of dictionaries in a for loop and checking for the desired value in each dictionary. When a match is found, we return the index of that dictionary in the list and exit the loop.

```python
def find_index(lst: list, key: str, value: any) -> int:
    for i, d in enumerate(lst):
        if d.get(key) == value:
            return i
    return -1        
```

In this example, we define a function `find_index` that takes three parameters: the list of dictionaries `lst` we want to search in, the key `key` we want to match the value against, and the value `value` we want to find. We use `enumerate` to get both the index and the current dictionary in each iteration of the loop.

If the value of `key` in the current dictionary matches `value`, we return the index `i` of that dictionary. If we exhaust the list without finding a match, the function returns `-1`.

## Solution approach 2: Using a list comprehension

Another approach is using a list comprehension to create a list of indices where the value of `key` matches `value`. Then, we can return the first element of that list if it's not empty, or `-1` otherwise.

```python
def find_index(lst: list, key: str, value: any) -> int:
    indices = [i for i, d in enumerate(lst) if d.get(key) == value]
    return indices[0] if indices else -1
```

Here, we use a list comprehension to create the list `indices` of all indices where the value of `key` matches `value`. We return the first element of `indices` if it's not empty, or `-1` if the list is empty.

## Conclusion

In this solution guide, we presented two approaches to find the index of a dict within a list, by matching the dict's value in Python. Both solutions are simple and easy to understand, but they may differ in their performance depending on the size of the list and the specific requirements of the problem. When in doubt, it's always a good idea to test both solutions and choose the one that performs better.
