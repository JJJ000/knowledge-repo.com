---
title: What is the method to merge two sets into a single line without employing the symbol "|" ?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `union` operator to combine the two sets into a new set.
---

**Contents**

[TOC]

Introduction:

Joining two sets in one line without using "|" in Python is a common task. In this tutorial, we will discuss how to achieve this task using various methods.

Method 1: Using 'union' method

In Python, we can use the 'union' method to combine two sets into a single set. The 'union' method returns a new set that contains all the items from both sets. Here is an example:

```
set1 = {1, 2, 3}
set2 = {4, 5, 6}
set3 = set1.union(set2)
print(set3)
```

Output: {1, 2, 3, 4, 5, 6}

Method 2: Using 'update' method

Another way to combine two sets in Python is to use the 'update' method. The 'update' method adds all the elements from one set to another set. Here is an example:

```
set1 = {1, 2, 3}
set2 = {4, 5, 6}
set1.update(set2)
print(set1)
```

Output: {1, 2, 3, 4, 5, 6}

Method 3: Using unpacking operator

We can also use the unpacking operator (*) to combine two sets in Python. The unpacking operator (*) unpacks the items in a set and passes them as separate arguments to the function. Here is an example:

```
set1 = {1, 2, 3}
set2 = {4, 5, 6}
set3 = {*set1, *set2}
print(set3)
```

Output: {1, 2, 3, 4, 5, 6}

Method 4: Using set comprehension

Finally, we can use set comprehension to combine two sets in Python. Set comprehension is an elegant way to create a new set by looping over an iterable. Here is an example:

```
set1 = {1, 2, 3}
set2 = {4, 5, 6}
set3 = {x for x in set1.union(set2)}
print(set3)
```

Output: {1, 2, 3, 4, 5, 6}

Conclusion:

In this tutorial, we have discussed four different ways to combine two sets into a single set without using the '|' operator. These methods include using the 'union' method, the 'update' method, the unpacking operator (*), and set comprehension. All these methods are effective and can be used depending on your specific use case.
