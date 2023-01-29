---
title: What is the best way to arrange a dictionary according to its keys?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the built-in sorted() function to sort a dictionary by key.
---

**Contents**

[TOC]

# Option 1 - Using the sorted() Function

The `sorted()` function can be used to sort a dictionary by key. The function takes in the dictionary to be sorted and returns a list of tuples sorted by key.

Example:

```
my_dict = {'a':1, 'b':2, 'c':3}

sorted_dict = sorted(my_dict.items())

print(sorted_dict)
# Output: [('a', 1), ('b', 2), ('c', 3)]
```

# Option 2 - Using the sorted() Method

The `dict` object has a `sorted()` method which can be used to sort a dictionary by key. The method returns a list of tuples sorted by key.

Example:

```
my_dict = {'a':1, 'b':2, 'c':3}

sorted_dict = my_dict.sorted()

print(sorted_dict)
# Output: [('a', 1), ('b', 2), ('c', 3)]
```

# Option 3 - Using the sorted() Function with the lambda Expression

The `sorted()` function can be used with a `lambda` expression to sort a dictionary by key. The `lambda` expression takes in the item and returns the key.

Example:

```
my_dict = {'a':1, 'b':2, 'c':3}

sorted_dict = sorted(my_dict.items(), key=lambda x: x[0])

print(sorted_dict)
# Output: [('a', 1), ('b', 2), ('c', 3)]
```

# Option 4 - Using the OrderedDict

The `collections` module has an `OrderedDict` class which can be used to sort a dictionary by key. The `OrderedDict` constructor takes in keyword arguments and returns an ordered dictionary.

Example:

```
from collections import OrderedDict

my_dict = {'a':1, 'b':2, 'c':3}

sorted_dict = OrderedDict(sorted(my_dict.items()))

print(sorted_dict)
# Output: OrderedDict([('a', 1), ('b', 2), ('c', 3)])
```
