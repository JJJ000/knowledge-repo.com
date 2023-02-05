---
title: Why doesn't the list data structure have a secure "get" method like the dictionary data structure does?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: List does not have a key-value structure like dictionary, so it does not have a safe `get` method.
---

**Contents**

[TOC]

# Reasons
1. Lists and dictionaries are different data structures, and they are used in different ways. 
2. Lists are ordered collections of elements, while dictionaries are unordered collections of key-value pairs. 

# Lists
1. Lists are designed to be used for sequential access. 
2. Accessing elements in a list by index is the most efficient way to access them. 

# Dictionaries
1. Dictionaries are designed for random access. 
2. The key-value pairs allow for efficient lookup of values by key. 

# Conclusion
1. Since lists are designed for sequential access, a safe "get" method would not be as efficient as simply accessing elements by index. 
2. On the other hand, dictionaries are designed for random access, so a safe "get" method is necessary to ensure that the correct value is returned.
