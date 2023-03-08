---
title: If a key is not present in a dictionary, Python will update it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `setdefault()` method to update a key in a dictionary if it doesn`t exist.
---

**Contents**

[TOC]

## Checking if key exists in dict

To update a key in a dictionary if it doesn't exist, we first need to check if the key already exists in the dictionary. We can do this using the `in` keyword or the `get` method.

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}

if 'key1' in my_dict:
    # key exists, update value
    my_dict['key1'] = 'new value'
else:
    # key does not exist, add key-value pair
    my_dict['key1'] = 'new value'
```

or

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}

if my_dict.get('key1') is not None:
    # key exists, update value
    my_dict['key1'] = 'new value'
else:
    # key does not exist, add key-value pair
    my_dict['key1'] = 'new value'
```

Both of these methods check if the key `'key1'` exists in the dictionary `my_dict`. If it does, the value is updated. If it doesn't, a new key-value pair is added to the dictionary.


## Using setdefault method

Python provides a `setdefault` method that can be used to add a new key-value pair to a dictionary if the key does not exist.

```python
my_dict = {'key1': 'value1', 'key2': 'value2'}

my_dict.setdefault('key1', 'new value')
```

If the key `'key1'` already exists in the dictionary, this does nothing. If the key `'key1'` does not exist in the dictionary, a new key-value pair `'key1': 'new value'` is added to the dictionary.


## Using defaultdict

Another approach is to use the `defaultdict` class from the `collections` module. This class provides a default value for keys that do not exist in the dictionary.

```python
from collections import defaultdict

my_dict = defaultdict(str)

my_dict['key1'] = 'value1'
my_dict['key2'] = 'value2'
my_dict['key1'] = 'new value'
my_dict['key3'] = 'value3'

print(my_dict)
```

Output:

```
defaultdict(<class 'str'>, {'key1': 'new value', 'key2': 'value2', 'key3': 'value3'})
```

In this example, we create a `defaultdict` with a default value of an empty string. We can then add new key-value pairs to the dictionary as usual. If a key does not exist, it is automatically created with the default value. If the key already exists, its value is updated as usual.
