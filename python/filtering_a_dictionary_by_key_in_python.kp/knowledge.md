---
title: Create a new dict containing only the desired keys from the original dict
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the dictionary`s pop() or popitem() method to remove unwanted keys from the dictionary.
---

**Contents**

[TOC]

#### Creating a Filtered Dictionary

To create a dictionary containing only certain keys, we can use a dictionary comprehension. This involves creating a new dictionary from an existing dictionary, filtering out unwanted keys as we go.

For example, if we have a dictionary `d` with the following key-value pairs:

```python
d = {
    'a': 1,
    'b': 2,
    'c': 3,
    'd': 4
}
```

We can create a new dictionary containing only the keys `a` and `c` with the following dictionary comprehension:

```python
filtered_dict = {k: v for k, v in d.items() if k in ['a', 'c']}
```

The resulting dictionary will be:

```python
filtered_dict = {
    'a': 1,
    'c': 3
}
```

#### Using the `dict.pop()` Method

Another way to filter a dictionary to contain only certain keys is to use the `dict.pop()` method. This method removes a key-value pair from a dictionary and returns the corresponding value.

For example, if we have a dictionary `d` with the following key-value pairs:

```python
d = {
    'a': 1,
    'b': 2,
    'c': 3,
    'd': 4
}
```

We can create a new dictionary containing only the keys `a` and `c` with the following code:

```python
filtered_dict = {}
filtered_dict['a'] = d.pop('a')
filtered_dict['c'] = d.pop('c')
```

The resulting dictionary will be:

```python
filtered_dict = {
    'a': 1,
    'c': 3
}
```

#### Using the `dict.update()` Method

Another way to filter a dictionary to contain only certain keys is to use the `dict.update()` method. This method updates the contents of a dictionary with the contents of another dictionary.

For example, if we have two dictionaries `d` and `filtered_dict` with the following key-value pairs:

```python
d = {
    'a': 1,
    'b': 2,
    'c': 3,
    'd': 4
}

filtered_dict = {}
```

We can update `filtered_dict` to contain only the keys `a` and `c` with the following code:

```python
filtered_dict.update({k: v for k, v in d.items() if k in ['a', 'c']})
```

The resulting dictionary will be:

```python
filtered_dict = {
    'a': 1,
    'c': 3
}
```
