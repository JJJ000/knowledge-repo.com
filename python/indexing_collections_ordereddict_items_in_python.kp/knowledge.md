---
title: Retrieving elements from a collections.ordereddict based on their position in the sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Items in an OrderedDict can be accessed by index using the key or by converting the OrderedDict to a list and accessing the item by index.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides a rich library of built-in data structures that make it easier to work with data. One of those data structures is the collections.OrderedDict, which is a dictionary subclass that remembers the order of items inserted. This makes it ideal for scenarios where we need to maintain the order of elements in a collection. In this tutorial, we'll explore how to access elements in an OrderedDict by index in Python.

Section 2: Creating an OrderedDict
Before we can access elements in an OrderedDict by index, we first need to create an instance of the OrderedDict class. To do this, we need to import the collections module and call the OrderedDict constructor method, as shown below:
```
import collections

od = collections.OrderedDict()
```
This creates an empty OrderedDict instance that we can use to store elements in an ordered manner.

Section 3: Accessing Elements by Index
Accessing elements in an OrderedDict by index is fairly simple in Python. We can use the indexing operator [] to access elements at a specific position in the OrderedDict. For instance, to access the first element in the OrderedDict, we can do the following:
```
import collections

od = collections.OrderedDict([
        ('apple', 1),
        ('banana', 2),
        ('orange', 3),
        ('pear', 4)
])

first_item = od[list(od)[0]]
print("First item: ", first_item)
```
In the above code, we created an OrderedDict with four elements and assigned it to the variable od. We then used the list() function to convert the OrderedDict into a list of tuples that preserve the order of the elements. We then accessed the first item by using the indexing operator [] and providing the index of the first item, which is 0.

Section 4: Conclusion
In this tutorial, we've demonstrated how to access items in an OrderedDict by index in Python. We've shown that we can create an OrderedDict instance using the collections module and access items using the indexing operator []. We hope this tutorial has been helpful in improving your Python skills.
