---
title: In what situations is it more appropriate to use iteritems() rather than items()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: `iteritems()` should be used instead of `items()` when working with large datasets in Python 2.x to avoid excessive memory usage. (Note `iteritems()` is no longer available in Python 3.x)
---

**Contents**

[TOC]

### When Key-Value Pairs are Large in Number

One scenario when `iteritems()` should be preferred over `items()` is when dealing with large dictionaries that contain a large number of key-value pairs. The reason is that `items()` creates and returns a list that contains all the key-value pairs, while `iteritems()` returns an iterator object that can be used to iterate over the key-value pairs one at a time. This approach saves memory and time as the entire list doesn't need to be created in memory at once.

### When Memory is Limited

Another scenario where `iteritems()` should be used over `items()` is when there is limited memory available. As stated above, `items()` creates and returns a list object containing all the key-value pairs in a dictionary. If the dictionary is very large, the list can consume a significant amount of memory. `iteritems()` on the other hand returns an iterator object that can be used to access the key-value pairs one at a time. This approach consumes less memory since only one key-value pair is accessed at any given time. 

### When Iterating Over Large DataSets

When working with large datasets where memory can be a limiting factor, `iteritems()` can also be leveraged to make the iteration process faster as we can get the items on-the-fly instead of loading them into the memory first. The same memory saving concept applies here, as using `iteritems()` helps us to append individual items in a list as we read them, rather than to store all the items in a list before processing. 

### When the Order is Not Important

If the order of the key-value pairs does not matter, then `iteritems()` can be used over `items()`. Iterating over an unordered dictionary with `iteritems()` can be way faster than doing so with `items()`. This is because the `iteritems()` approach does not need to use extra memory to keep the order of the key-value pairs while iterating over.
