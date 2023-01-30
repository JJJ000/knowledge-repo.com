---
title: What is the syntax for converting the keys of a dictionary to a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the built-in list() function to return a list of dictionary keys.
---

**Contents**

[TOC]

# Section 1: Using the .keys() Method

The .keys() method is used to return the dictionary's keys as a list. 

Example: 

```
my_dict = {'name': 'John', 'age': 32, 'city': 'New York'}
key_list = list(my_dict.keys())
print(key_list)

Output: ['name', 'age', 'city']
```

# Section 2: Using the dict.items() Method

The dict.items() method can also be used to return the dictionary's keys as a list.

Example:

```
my_dict = {'name': 'John', 'age': 32, 'city': 'New York'}
key_list = list(my_dict.items())
print(key_list)

Output: [('name', 'John'), ('age', 32), ('city', 'New York')]
```

# Section 3: Using a for Loop

A for loop can also be used to return the dictionary's keys as a list.

Example:

```
my_dict = {'name': 'John', 'age': 32, 'city': 'New York'}
key_list = []
for key in my_dict:
    key_list.append(key)
print(key_list)

Output: ['name', 'age', 'city']
```

# Section 4: Using List Comprehension

List comprehension can also be used to return the dictionary's keys as a list.

Example:

```
my_dict = {'name': 'John', 'age': 32, 'city': 'New York'}
key_list = [key for key in my_dict]
print(key_list)

Output: ['name', 'age', 'city']
```
