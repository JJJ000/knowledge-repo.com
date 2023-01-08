---
title: What are the distinctions between __str__ and __repr__?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: __str__ is used to create a human-readable representation of an object, while __repr__ is used to create a machine-readable representation of an object.
---

**Contents**

[TOC]

### `__str__`
The `__str__` method is used to return a human-readable string representation of an object. It is used to provide a “pretty print” of the object’s state. It is called when a string representation of an object is needed, such as when a print statement is used.

### `__repr__`
The `__repr__` method is used to return a string representation of an object. It is used to provide an unambiguous representation of the object’s state and is used for debugging and logging purposes. It is called when an “official” string representation of an object is needed, such as for printing in the interactive interpreter.

### Difference
The main difference between `__str__` and `__repr__` is that `__str__` is used to provide a “pretty print” of the object’s state, while `__repr__` is used to provide an unambiguous representation of the object’s state.
