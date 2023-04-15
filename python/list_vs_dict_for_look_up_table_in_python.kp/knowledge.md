---
title: What's better for look up table - list or dict in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Dict is better for look up table as it provides faster access compared to list.
---

**Contents**

[TOC]

Overview:
Lists and dictionaries are two common types of data structures in Python. Lists are ordered collections of elements whereas dictionaries are unordered collections of key-value pairs. When it comes to creating a lookup table, both lists and dictionaries can be used. Here are some factors to consider when deciding between a list and a dictionary for a lookup table.

1. Flexibility and Ease of Access
Dictionaries are great for creating lookup tables because they offer flexibility and ease of access. With a dictionary, you can easily look up a value based on its key, which can be a string, integer, or any other hashable data type. This makes dictionaries ideal for situations where you need to quickly retrieve a value based on a specific identifier. In the case of non-hashable items a list may be preferred.

2. Memory Footprint
Lists are generally more memory-efficient than dictionaries, especially when the number of elements is small. However, as the number of elements in a list grows, its memory footprint also grows, whereas the memory footprint of a dictionary remains constant regardless of the size. If you have a large number of elements in your lookup table, a dictionary may be a better choice to avoid overburdening your system's memory.

3. Lookup Time
The time it takes to look up an element in a list or dictionary depends on the size of the data structure. In general, dictionaries offer faster lookup times than lists, especially as the number of elements grows. This is because a dictionary's key is used to directly access the corresponding value, whereas with a list, you have to iterate through each element until you find the one you’re looking for.

4. Adding and Removing Elements
Adding and removing elements to/from a list is straightforward, whereas with a dictionary, there are a few additional considerations. If you add a new key-value pair to a dictionary, it will be inserted at an arbitrary position based on the hash value of the key. If you remove a key-value pair from a dictionary, the remaining elements may need to be rehashed, which can be a time-consuming operation. With a list, adding or removing elements can be done with simple append() and pop() operations.

Conclusion:
In conclusion, both lists and dictionaries can be used to create lookup tables, but the choice largely depends on the requirements of your application. If you need a data structure that offers flexibility and fast lookup times, a dictionary is the way to go. If memory footprint is a concern or you need a data structure that is easy to manipulate, a list may be a better choice.
