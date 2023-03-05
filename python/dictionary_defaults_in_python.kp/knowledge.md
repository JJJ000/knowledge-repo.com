---
title: The concept of default values in dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Dictionaries in Python allow for storing key-value pairs and accessing values using keys, and the setdefault() method can be used to establish default values for keys that are not present.
---

**Contents**

[TOC]

### Introduction to Dictionaries in Python

A dictionary is an unordered collection of key-value pairs, where each key is unique. In Python, dictionaries are implemented as hash tables, which make searching for a specific key very fast. To define a dictionary, you use curly braces {} and separate the key-value pairs with colons :

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}
```

Dictionaries are very useful whenever you need to store and manipulate data in a structured way, and they’re commonly used for representing JSON objects, configuration settings, and other similar structures.


### Accessing Values in a Dictionary

To access a value in a dictionary, you simply need to provide the corresponding key in square brackets. For example:

```python
my_dict = {'name': 'John', 'age': 30}

print(my_dict['name'])    # Output: 'John'
```

If the key doesn’t exist in the dictionary, Python will raise a KeyError.

```python
print(my_dict['height'])  # Raises: KeyError: 'height'
```

### Default Values in Dictionaries

When working with dictionaries, it’s often useful to have a default value to return if the key doesn’t exist in the dictionary. You can achieve this behavior by using the `get()` method and providing a default value as a second argument.

```python
my_dict = {'name': 'John', 'age': 30}

print(my_dict.get('name', 'unknown'))   # Output: 'John'
print(my_dict.get('height', 'unknown')) # Output: 'unknown'
```

If the key exists in the dictionary, `get()` will return its value. Otherwise, it will return the default value provided in the second argument.


### Setting Default Values for Dictionaries

If you’re working with dictionaries that have deeply nested structures, it can be useful to use defaultdict instead of a regular dictionary. defaultdict is a subclass of dict that overrides one method to provide a default value for missing keys. 

```python
from collections import defaultdict

my_dict = defaultdict(list)

my_dict['names'].append('John')
my_dict['names'].append('Susan')

print(my_dict)  # Output: defaultdict(<class 'list'>, {'names': ['John', 'Susan']})
```

In this example, `defaultdict(list)` creates a dictionary with default values of empty lists [] whenever a missing key is accessed. By using `my_dict['names'].append('John')`, we’re able to add multiple values to the same key without having to initialize it first.
