---
title: What does it mean if an object in Python can be accessed using brackets?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: If an object is subscriptable, it means that it can be indexed using square brackets, like an array or list.
---

**Contents**

[TOC]

### Definition

Subscriptable objects in Python are objects that can be indexed, sliced, and iterated over. This means that the object can be indexed using square brackets (e.g. `obj[0]`) or sliced using a colon (e.g. `obj[2:4]`). Iteration over subscriptable objects can be done using a `for` loop (e.g. `for i in obj:`).

### Examples

Common examples of subscriptable objects in Python are strings, lists, and dictionaries. Strings can be indexed or sliced to access individual characters, lists can be indexed or sliced to access individual elements, and dictionaries can be indexed to access individual values.

### Non-Subscriptable Objects

Not all objects in Python are subscriptable. For example, integers and floats are not subscriptable, as they cannot be indexed or sliced. Additionally, some objects, such as sets, may not be subscriptable depending on the implementation.
