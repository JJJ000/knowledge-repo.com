---
title: How can the list [key1,val1,key2,val2] be transformed into a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Using the built-in zip function and passing the list to the dict constructor. 

Example dict(zip([key1, val1, key2, val2]))
---

**Contents**

[TOC]

## Introduction
In Python, we can convert a list of key-value pairs to a dictionary. This is especially useful when we have data in the form of a list but want to convert it to a dictionary for easier manipulation or data analysis. Here, I will demonstrate how to convert a key-value list to a dictionary in Python.

## Converting a key-value list to a dictionary using a loop
One way to convert a key-value list to a dictionary is by using a loop. We can iterate over the list two items at a time, where the first item is the key and the second item is the value. We can then add these key-value pairs to an empty dictionary using square bracket notation. Here is an example:

```
my_list = ['key1', 'val1', 'key2', 'val2']
my_dict = {}
for i in range(0, len(my_list), 2):
    key = my_list[i]
    val = my_list[i+1]
    my_dict[key] = val
print(my_dict)
```

Output:
```
{'key1': 'val1', 'key2': 'val2'}
```

## Converting a key-value list to a dictionary using dictionary comprehension
Another way to convert a key-value list to a dictionary is by using dictionary comprehension. In this method, we can iterate over the list two items at a time, and use dictionary comprehension to create a dictionary from these pairs. Here is an example:

```
my_list = ['key1', 'val1', 'key2', 'val2']
my_dict = {my_list[i]: my_list[i+1] for i in range(0, len(my_list), 2)}
print(my_dict)
```

Output:
```
{'key1': 'val1', 'key2': 'val2'}
```

## Conclusion
In this tutorial, I have shown how to convert a key-value list to a dictionary in Python using both a loop and dictionary comprehension. Both methods are simple and efficient for converting lists to dictionaries depending on your preferences.
