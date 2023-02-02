---
title: What are the distinctions between np.array() and np.asarray()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: np.array() creates a new array, while np.asarray() converts an existing array or object into an array.
---

**Contents**

[TOC]

### np.array()

np.array() is used to create a new array from an existing array or a list of objects. It takes the object as a parameter and returns an array of the same type as the object. The new array created by np.array() is a copy of the original object.

### np.asarray()

np.asarray() is used to convert an existing array or list of objects into an array. Unlike np.array(), np.asarray() does not create a new array, but instead returns a reference to the original object. This means that any changes made to the returned array will also be reflected in the original object.
