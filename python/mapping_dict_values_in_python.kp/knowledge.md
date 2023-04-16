---
title: Iterating through the items in a Python dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the dict.values() method to iterate over the values in a dictionary and use a for loop to map a function over the values.
---

**Contents**

[TOC]

##### Using for loop

We can use a `for` loop to iterate over the key-value pairs in a dictionary. For example:

```python
my_dict = {'a':1, 'b':2, 'c':3}

for key, value in my_dict.items():
    print(key, value)
```

##### Using dict.values()

We can also use the `dict.values()` method to iterate over the values in a dictionary. For example:

```python
my_dict = {'a':1, 'b':2, 'c':3}

for value in my_dict.values():
    print(value)
```

##### Using dict.items()

We can use the `dict.items()` method to iterate over the key-value pairs in a dictionary. For example:

```python
my_dict = {'a':1, 'b':2, 'c':3}

for key, value in my_dict.items():
    print(key, value)
```

##### Using dict.keys()

We can use the `dict.keys()` method to iterate over the keys in a dictionary. For example:

```python
my_dict = {'a':1, 'b':2, 'c':3}

for key in my_dict.keys():
    print(key)
```
