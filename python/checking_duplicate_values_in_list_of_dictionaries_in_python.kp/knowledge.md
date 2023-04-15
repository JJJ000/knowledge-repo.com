---
title: Can you verify whether the value is already present in the list of dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use a loop to iterate through the list of dictionaries and check if the value exists in one of the dictionaries using the `in` keyword.
---

**Contents**

[TOC]

## Problem Statement

Suppose we have a list of dictionaries in Python and we want to check if a particular value exists in any of the dictionaries within the list. How can we achieve this?


## Approach

We can loop through each dictionary in the list and check if the value exists as a key in the dictionary or as a value associated with any of the keys in the dictionary. If the value is found in any of the dictionaries, we can return `True` indicating that the value already exists within the list of dictionaries.


## Pseudo Code

```
def is_value_present(list_of_dicts, value_to_check):
    for dictionary in list_of_dicts:
        if value_to_check in dictionary.values() or value_to_check in dictionary.keys():
            return True
    return False
```


## Python code

```python
def is_value_present(list_of_dicts, value_to_check):
    """
    This function takes a list of dictionaries and a value to check as input parameters.
    It returns True if the value already exists within any of the dictionaries in the list, else False.
    """
    for dictionary in list_of_dicts:
        if value_to_check in dictionary.values() or value_to_check in dictionary.keys():
            return True
    return False
```
