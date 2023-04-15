---
title: What is the most efficient way to combine two lists in Python without changing either one?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the `+` operator to concatenate two lists without modifying either one.
---

**Contents**

[TOC]

# Section 1: Using + Operator

The simplest way to get the concatenation of two lists without modifying either one is to use the `+` operator. This operator can be used to concatenate two lists and return a new list, without modifying the original lists.

Example: 
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list1 + list2

print(list3)
# Output: [1, 2, 3, 4, 5, 6]
```

# Section 2: Using extend() Method

Another way to get the concatenation of two lists without modifying either one is to use the `extend()` method. This method can be used to add the elements of one list to the end of another list, without modifying the original lists.

Example: 
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.extend(list2)

print(list1)
# Output: [1, 2, 3, 4, 5, 6]
```

# Section 3: Using itertools.chain()

The `itertools.chain()` function can also be used to get the concatenation of two lists without modifying either one. This function takes two or more iterable objects and returns a single iterable object that contains all the elements of the input iterables.

Example: 
```
from itertools import chain

list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list(chain(list1, list2))

print(list3)
# Output: [1, 2, 3, 4, 5, 6]
```

# Section 4: Using + Operator with List Comprehension

The `+` operator can also be used with list comprehension to get the concatenation of two lists without modifying either one. This approach allows us to create a new list by combining the elements of two lists without modifying the original lists.

Example: 
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = [x for x in list1] + [y for y in list2]

print(list3)
# Output: [1, 2, 3, 4, 5, 6]
```
