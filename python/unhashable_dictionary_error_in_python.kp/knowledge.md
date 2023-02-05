---
title: It is not possible to use a dictionary as a key in a dictionary, as dictionaries are mutable and therefore cannot be hashed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A dict is not a hashable type in Python and cannot be used as a key in a dictionary.
---

**Contents**

[TOC]

# Introduction
A TypeError: unhashable type: 'dict' in Python is an error that occurs when a dictionary is used as a key in a dictionary. This error occurs because dictionaries are mutable objects and cannot be used as keys in a dictionary.

# Reason for Error
The reason for this error is that dictionaries are mutable objects, meaning that their values can be changed after they have been created. Since dictionaries are not immutable, they cannot be used as keys in a dictionary.

# Solutions
To solve this error, you can either convert the dictionary to an immutable object such as a tuple or use an alternative data structure such as a list or set.

# Conclusion
In conclusion, a TypeError: unhashable type: 'dict' in Python occurs when a dictionary is used as a key in a dictionary. This error is caused by the fact that dictionaries are mutable objects and cannot be used as keys in a dictionary. To solve this error, you can either convert the dictionary to an immutable object or use an alternative data structure.
