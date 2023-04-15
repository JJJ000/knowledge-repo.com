---
title: What is the syntax for combining two lists in Python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can concatenate two lists in Python by using the '+' operator.
---

**Contents**

[TOC]

### Using the "+" Operator

The "+" operator can be used to concatenate two lists in Python. For example:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list1 + list2

print(list3)
# Output: [1, 2, 3, 4, 5, 6]
```

### Using the extend() Method

The extend() method can be used to add all the elements of one list to another list. For example:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.extend(list2)

print(list1)
# Output: [1, 2, 3, 4, 5, 6]
```

### Using the append() Method

The append() method can be used to add a single element to the end of a list. This method can be used in a loop to concatenate two lists. For example:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

for element in list2:
    list1.append(element)

print(list1)
# Output: [1, 2, 3, 4, 5, 6]
```

### Using the itertools.chain() Method

The itertools.chain() method can be used to concatenate two lists. This method takes two iterables as arguments and returns an iterator that yields the elements of the first iterable followed by the elements of the second iterable. For example:

```python
import itertools

list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list(itertools.chain(list1, list2))

print(list3)
# Output: [1, 2, 3, 4, 5, 6]
```
