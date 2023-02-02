---
title: What is the first key in a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the dictionary`s `get()` method to retrieve the first key.
---

**Contents**

[TOC]

# Accessing Keys
The first key in a dictionary can be accessed by using the `dictionary.keys()` method. This method returns a list of all the keys in the dictionary.

# Indexing the List
The first key in the list can then be accessed by indexing the list. Since the first item in the list is at index 0, the first key can be accessed by using `dictionary.keys()[0]`.

# Accessing Values
The value associated with the first key can be accessed by using the syntax `dictionary[dictionary.keys()[0]]`. This will return the value associated with the first key in the dictionary.
