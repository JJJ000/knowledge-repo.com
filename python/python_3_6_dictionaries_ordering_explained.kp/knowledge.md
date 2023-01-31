---
title: What is the ordering of items in a dictionary in Python 3.6 and later?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: No, dictionaries are unordered in Python 3.6+.
---

**Contents**

[TOC]

# Yes

Python 3.6+ dictionaries are ordered data structures. This means that the items in the dictionary maintain their insertion order.

# How

The ordering of a dictionary is based on the hash values of the keys. When a new item is added to the dictionary, it is assigned a hash value and stored in the order of its hash value.

# Benefits

The ordering of dictionaries allows for faster lookups because the items can be accessed in the order they are stored. This is beneficial for applications that require quick access to data. Additionally, the ordering allows for easier iteration over the dictionary.
