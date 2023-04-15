---
title: Could you enumerate the base classes in the hierarchy of a specified class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `\_\_bases\_\_` attribute of the class to retrieve a tuple of all direct parent classes in the hierarchy.
---

**Contents**

[TOC]

## Get the Base Classes

To get the base classes of a given class in Python, we can use the `__bases__` attribute. This attribute returns a tuple of base classes in order of their occurrence in the class hierarchy.


## Example

Let's consider a class hierarchy as follows:

```
class A:
    pass

class B(A):
    pass

class C(A):
    pass

class D(B, C):
    pass
```

To get the base classes of `D`, we can call `D.__bases__` which will return a tuple:

```
(<class '__main__.B'>, <class '__main__.C'>)
```


## Printing the Base Classes

To print the base classes in a more readable format, we can loop through the `__bases__` tuple and print out each class name using the `__name__` attribute.


## Example

Using the same class hierarchy as before, we can print the base classes of `D` as follows:

```
base_classes = D.__bases__
for base_class in base_classes:
    print(base_class.__name__)
```

This will output:

```
B
C
```
