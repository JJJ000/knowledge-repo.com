---
title: Swap the keys and values of a dictionary mapping
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: A dictionary mapping can be reversed or inverted in Python by using the built-in dict() constructor and passing in the original dictionary as the argument.
---

**Contents**

[TOC]

#### Using a Dictionary Comprehension

A dictionary comprehension can be used to invert a dictionary mapping. This involves creating a new dictionary with the keys and values of the original dictionary swapped. 

```python
original_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
inverted_dict = {value: key for key, value in original_dict.items()}

print(inverted_dict)
# {1: 'a', 2: 'b', 3: 'c', 4: 'd'}
```

#### Using the zip() Function

The zip() function can also be used to invert a dictionary mapping. This involves creating a list of tuples containing the keys and values of the original dictionary, then creating a new dictionary from the list of tuples. 

```python
original_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
inverted_dict = dict(zip(original_dict.values(), original_dict.keys()))

print(inverted_dict)
# {1: 'a', 2: 'b', 3: 'c', 4: 'd'}
```

#### Using the invert() Method

The invert() method can be used to invert a dictionary mapping. This method is available in Python 3.8 and above. 

```python
original_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
inverted_dict = original_dict.invert()

print(inverted_dict)
# {1: 'a', 2: 'b', 3: 'c', 4: 'd'}
```

#### Using the collections.defaultdict() Method

The collections.defaultdict() method can also be used to invert a dictionary mapping. This involves creating a new default dictionary with the values of the original dictionary as keys and the keys of the original dictionary as values. 

```python
from collections import defaultdict

original_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
inverted_dict = defaultdict(list)

for key, value in original_dict.items():
    inverted_dict[value].append(key)

print(inverted_dict)
# defaultdict(<class 'list'>, {1: ['a'], 2: ['b'], 3: ['c'], 4: ['d']})
```
