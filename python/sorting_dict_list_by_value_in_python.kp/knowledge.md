---
title: What is the best way to arrange a list of dictionaries based on a specific value within the dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the sorted() function with the key argument set to the key of the dictionary to sort a list of dictionaries by a value of the dictionary.
---

**Contents**

[TOC]

# Section 1: Creating a List of Dictionaries

A list of dictionaries can be created by defining a list of dictionaries in the following format:

```
list_of_dicts = [
    {'key1': 'value1', 'key2': 'value2', ...}, 
    {'key1': 'value3', 'key2': 'value4', ...}, 
    ...
]
```

# Section 2: Sorting the List of Dictionaries

The `sorted()` function can be used to sort the list of dictionaries according to the value of a given key. 

For example, to sort the list of dictionaries by the value of the key 'key1':

```
sorted_list_of_dicts = sorted(list_of_dicts, key=lambda k: k['key1'])
```

# Section 3: Descending Order

To sort the list of dictionaries in descending order, the `reverse` parameter can be set to `True`:

```
sorted_list_of_dicts = sorted(list_of_dicts, key=lambda k: k['key1'], reverse=True)
```

# Section 4: Multiple Keys

To sort the list of dictionaries by multiple keys, the `sorted()` function can be called multiple times in succession:

```
sorted_list_of_dicts = sorted(list_of_dicts, key=lambda k: k['key1'])
sorted_list_of_dicts = sorted(sorted_list_of_dicts, key=lambda k: k['key2'])
```
