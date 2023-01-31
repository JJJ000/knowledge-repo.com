---
title: How do dict.items() and dict.iteritems() differ in python2?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: dict.items() returns a list of key-value pairs, while dict.iteritems() returns an iterator over the key-value pairs.
---

**Contents**

[TOC]

##### Functionality
dict.items() returns a list of key-value pairs in the form of tuples. dict.iteritems() returns an iterator object that can be used to loop over the key-value pairs.

##### Performance
dict.items() is more efficient in terms of memory usage, as it returns all the key-value pairs at once. dict.iteritems() is more efficient in terms of time, as it returns the key-value pairs one at a time, which can be useful for large dictionaries.

##### Syntax
dict.items() is used with the syntax dict.items(). dict.iteritems() is used with the syntax dict.iteritems().

##### Compatibility
dict.items() is compatible with both Python2 and Python3. dict.iteritems() is only compatible with Python2.
