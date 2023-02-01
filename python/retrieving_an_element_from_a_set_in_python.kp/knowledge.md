---
title: How can I access an element from a set without taking it out?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the set`s `in` operator to check if an element is in the set, or use the set`s `get` method to retrieve an element without removing it.
---

**Contents**

[TOC]

# Using the `.discard()` Method
The `.discard()` method can be used to retrieve an element from a set without removing it. The syntax is as follows:
```
set_name.discard(element)
```

# Example
For example, let's say we have a set called `my_set` with the following elements:
```
my_set = {1, 2, 3, 4, 5}
```

We can retrieve the element `3` without removing it from the set using the `.discard()` method as follows:
```
my_set.discard(3)
```

The element `3` will be retrieved from the set, but the set will remain unchanged.

# Return Value
The `.discard()` method does not return any value.
