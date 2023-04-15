---
title: How can I use one list to index another list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use list comprehension or a for loop to iterate over the indices of the second list and use those indices to access elements in the first list.
---

**Contents**

[TOC]

Section 1: Introduction
To index a list with another list in Python, we need to understand list slicing and indexing. List slicing is used to extract a range of elements from a list.

Section 2: Indexing a List with Another List
To index a list with another list, we can use list comprehension.
Here’s an example:

```
list1 = ["apple", "banana", "orange", "grape"]
index_list = [0, 2]

new_list = [list1[i] for i in index_list]
print(new_list)
```

In this example, we have two lists, list1 and index_list. We want to extract the elements at index positions 0 and 2 in list1.

We use list comprehension to create a new list that contains the elements at the index positions specified in index_list.

The output will be:
```
['apple', 'orange']
```

Section 3: Using a Loop
Alternatively, we can use a loop to index a list with another list.

```
list1 = ["apple", "banana", "orange", "grape"]
index_list = [0, 2]

new_list = []
for i in index_list:
    new_list.append(list1[i])
print(new_list)
```

This code creates a new empty list called new_list. Then, it loops through the index_list and appends the elements from list1 that correspond to the index positions in index_list.

The output will be:
```
['apple', 'orange']
```

Section 4: Conclusion
Indexing a list with another list is a common task in Python. Using list comprehension or a loop provides us with options to extract the desired elements from one list based on the elements in another list.
