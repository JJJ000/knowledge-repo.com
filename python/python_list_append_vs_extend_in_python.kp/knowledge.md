---
title: How do Python's list methods append and extend differ?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: The append() method adds an item to the end of the list, while the extend() method adds all items from an iterable to the end of the list.
---

**Contents**

[TOC]

### Append

The `append` method adds an item to the end of a list. It takes one argument, which can be any type of object (string, number, list, etc.). This method does not return a new list; it modifies the original list.

### Extend

The `extend` method adds all items from an iterable (list, tuple, string, etc.) to the end of a list. It takes one argument, which must be an iterable object. This method does not return a new list; it modifies the original list. Unlike `append`, `extend` adds each item from the iterable object individually, rather than adding the iterable object as a single item.
