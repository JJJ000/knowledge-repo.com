---
title: Searching for and replacing items in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To find and replace elements in a list in Python, use the list`s index and the assignment operator (=).
---

**Contents**

[TOC]

### Finding Elements

Finding elements in a list can be done with the `in` keyword. This keyword can be used to check if an element is present in a list.

For example:

```python
my_list = [1, 2, 3, 4, 5]

if 3 in my_list:
    print("3 is in the list")
```

### Replacing Elements

Replacing elements in a list can be done with the `list.insert()` and `list.remove()` methods. 

The `list.insert()` method takes two arguments - the index of the element to be replaced and the new element.

For example:

```python
my_list = [1, 2, 3, 4, 5]

my_list.insert(2, 10)

print(my_list) # [1, 2, 10, 3, 4, 5]
```

The `list.remove()` method takes one argument - the element to be removed.

For example:

```python
my_list = [1, 2, 3, 4, 5]

my_list.remove(3)

print(my_list) # [1, 2, 4, 5]
```

### Replacing Multiple Elements

Replacing multiple elements in a list can be done with the `list.replace()` method. This method takes two arguments - the old elements to be replaced and the new elements to replace them with.

For example:

```python
my_list = [1, 2, 3, 4, 5]

my_list.replace([3, 4], [10, 11])

print(my_list) # [1, 2, 10, 11, 5]
```
