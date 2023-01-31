---
title: Searching a Python list for dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can search through a list of dictionaries by looping through the list and using the dictionary`s key-value pairs.
---

**Contents**

[TOC]

## 1. Understanding the Problem

The problem is to search a Python list of dictionaries. A list of dictionaries is a collection of dictionaries, which are collections of key-value pairs. To search a list of dictionaries, we need to iterate over the list and check each dictionary to see if it contains the desired key-value pair.

## 2. Pseudocode

The following pseudocode describes a search algorithm for a list of dictionaries:

```
for each dictionary in the list:
    for each key-value pair in the dictionary:
        if the key-value pair matches the desired search criteria:
            return the dictionary
```

## 3. Python Code

The following code implements the pseudocode described above:

```python
def search_list_of_dicts(list_of_dicts, key, value):
    for d in list_of_dicts:
        for k, v in d.items():
            if k == key and v == value:
                return d
```

## 4. Example

The following example shows how to use the `search_list_of_dicts` function:

```python
list_of_dicts = [
    {'name': 'John', 'age': 25},
    {'name': 'Jane', 'age': 20},
    {'name': 'Bob', 'age': 30},
]

result = search_list_of_dicts(list_of_dicts, 'name', 'Jane')

print(result)
# {'name': 'Jane', 'age': 20}
```
