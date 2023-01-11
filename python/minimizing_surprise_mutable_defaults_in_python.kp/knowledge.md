---
title: The principle of least surprise and the modifiable default argument
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Least Astonishment is a concept in Python programming that suggests that the default value of a mutable argument should not be changed unexpectedly.
---

**Contents**

[TOC]

### Definition

Least Astonishment is a software design principle that states that a software system should be designed in such a way that its behavior is as predictable and unsurprising as possible. The idea is that users should not be surprised by the behavior of a system, and that the system should behave in a way that is consistent with the user's expectations.

### Mutable Default Argument

In Python, a mutable default argument is an argument to a function that is defined with a default value that is a mutable object, such as a list or a dictionary. When a mutable default argument is used, the value of the argument is evaluated only once when the function is defined, and that same value is used for all subsequent calls to the function. This can lead to unexpected behavior, as the value of the argument may be changed by the function in a way that the user did not expect.

### Least Astonishment

The use of mutable default arguments can violate the Least Astonishment principle, as the behavior of the function may be unexpected and surprising to the user. To avoid this, it is generally recommended that mutable default arguments should be avoided, and that immutable default arguments (such as integers or strings) should be used instead. This will ensure that the behavior of the function is more predictable and unsurprising.
