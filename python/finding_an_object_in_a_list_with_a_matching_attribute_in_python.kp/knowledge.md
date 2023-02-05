---
title: Search the list for an item with an attribute that matches a specified value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the list comprehension syntax to find the object in the list that has an attribute equal to some value that meets any condition.
---

**Contents**

[TOC]

#Section 1: Overview
Python provides a number of ways to search for objects in a list that have attributes equal to some value. This includes using built-in functions such as `filter()` and `list comprehension`, as well as custom functions.

#Section 2: Built-in Functions
The `filter()` function can be used to search for objects in a list that have attributes equal to some value. This function takes a function and an iterable as arguments, and returns an iterator with the elements from the iterable for which the function returns `True`. For example:

```python
def find_by_attribute(list_of_objects, attribute, value):
    return filter(lambda x: getattr(x, attribute) == value, list_of_objects)

list_of_objects = [Object1, Object2, Object3]
attribute = "name"
value = "John"

filtered_objects = find_by_attribute(list_of_objects, attribute, value)
```

The `list comprehension` syntax can also be used to search for objects in a list that have attributes equal to some value. This syntax takes the form of `[expression for item in list if condition]` and returns a list of elements for which the condition is `True`. For example:

```python
list_of_objects = [Object1, Object2, Object3]
attribute = "name"
value = "John"

filtered_objects = [obj for obj in list_of_objects if getattr(obj, attribute) == value]
```

#Section 3: Custom Functions
A custom function can also be written to search for objects in a list that have attributes equal to some value. This function can take the list of objects, the attribute, and the value as arguments, and return a list of objects for which the attribute is equal to the value. For example:

```python
def find_by_attribute(list_of_objects, attribute, value):
  filtered_objects = []
  for obj in list_of_objects:
    if getattr(obj, attribute) == value:
      filtered_objects.append(obj)
  return filtered_objects

list_of_objects = [Object1, Object2, Object3]
attribute = "name"
value = "John"

filtered_objects = find_by_attribute(list_of_objects, attribute, value)
```

#Section 4: Conclusion
In summary, Python provides a number of ways to search for objects in a list that have attributes equal to some value. These include using built-in functions such as `filter()` and `list comprehension`, as well as custom functions.
