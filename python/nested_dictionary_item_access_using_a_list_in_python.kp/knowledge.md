---
title: Can you obtain the elements of a nested dictionary by using a list of keys?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use reduce() function with get() method to access nested dictionary items via a list of keys in Python.
---

**Contents**

[TOC]

## Section 1: Introduction

In Python, dictionaries can contain other dictionaries as well as lists of dictionaries. In such cases, it may be necessary to access specific deeply nested values within these structures using a list of keys. This can be done using a simple function that recursively traverses the dictionary, getting the value of each key in turn until the desired value is reached. 

## Section 2: Writing the Function

To achieve this, we can create a function that takes a dictionary and a list of keys, and returns the value of the final key in the list. If the dictionary does not contain the key, the function returns None. If the key is a dictionary itself, the function calls itself again with the new dictionary and the remaining keys in the list. Here is the code for such a function:

```python
def get_nested_value(d: dict, keys: list):
    if not keys:
        return d
    if keys[0] not in d:
        return None
    return get_nested_value(d[keys[0]], keys[1:])
```

Here, the function recursively calls itself with the item in the dictionary corresponding to the first key in the list, and the remaining keys in the list. This continues until either the end of the list is reached (returning the final value), or a key is not present in the current dictionary (returning None).

## Section 3: Using the Function

To use this function, we simply need to pass it a dictionary and a list of keys. For example:

```python
a = {'foo': {'bar': {'baz': 42}}}
keys = ['foo', 'bar', 'baz']
value = get_nested_value(a, keys)
print(value)
```

This would output the value `42`.

## Section 4: Conclusion

In conclusion, accessing deeply nested dictionary items via a list of keys can be accomplished in Python by writing a simple recursive function. This function can be called with any dictionary and list of keys, and will return the desired value if it exists in the dictionary.
