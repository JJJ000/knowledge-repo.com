---
title: The order of elements in a list alters when it is transformed into a set
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Yes, converting a list to a set may change the order of elements because sets are unordered collections of unique elements in Python.
---

**Contents**

[TOC]

# Overview

In Python, a list is an ordered collection of objects, whereas a set is an unordered collection of unique objects. When converting a list to a set, the order of elements is not preserved. This is because the primary feature of a set is that it does not contain any duplicate elements, and it is optimized for membership testing and set operations, rather than indexing and slicing.

# Example

Let's take a look at an example to illustrate this behavior:

```
my_list = [4, 1, 3, 5, 2]
my_set = set(my_list)

print(my_list)
print(my_set)
```

The output of this code snippet would be:

```
[4, 1, 3, 5, 2]
{1, 2, 3, 4, 5}
```

As you can see, the original order of elements in the list is not preserved in the resulting set.

# Why the order is not preserved

The reason why the order is not preserved when converting a list to a set is because sets in Python are implemented using a hash table, which does not maintain any specific order of elements. Instead, it uses a hash function to map each element to a unique slot in the table, based on its value. This makes it very efficient to check whether an element is in the set or not, but also means that the order of elements is not guaranteed.

# How to preserve order when converting a list to a set

If you need to preserve the order of elements when converting a list to a set, you can use a different data structure, such as an OrderedDict or a list with duplicate elements removed:

```
from collections import OrderedDict

my_list = [4, 1, 3, 5, 2]
my_ordered_dict = OrderedDict.fromkeys(my_list)
my_ordered_list = list(my_ordered_dict.keys())

print(my_ordered_dict)
print(my_ordered_list)
```

The output of this code snippet would be:

```
OrderedDict([(4, None), (1, None), (3, None), (5, None), (2, None)])
[4, 1, 3, 5, 2]
```

As you can see, the order of elements is preserved using an OrderedDict, which maintains the order of elements based on their insertion order. Alternatively, you can remove duplicate elements from a list using the built-in set() function, and then convert the resulting set back into a list:

```
my_list = [4, 1, 3, 5, 2, 1, 3, 5]
my_set = set(my_list)
my_ordered_list = list(my_set)

print(my_ordered_list)
```

The output of this code snippet would be:

```
[1, 2, 3, 4, 5]
```

As you can see, the duplicates have been removed, but the order of elements is preserved.
