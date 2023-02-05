---
title: What is the definition of "hashable" in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, `hashable` refers to an object that can be converted into a hash value or key, which can be used to uniquely identify it.
---

**Contents**

[TOC]

# Definition

In Python, a hashable object is an object that can be converted to a hash value, or a value that can be used as a dictionary key.

# Examples

Examples of hashable objects in Python include strings, tuples, integers, and floats.

# Benefits

Hashable objects are beneficial because they can be used as keys in dictionaries. This allows for efficient lookups and storage of data.

# Limitations

Hashable objects have certain limitations. For example, they cannot be changed once they are created. Additionally, some objects, such as lists and dictionaries, are not hashable.
