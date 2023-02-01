---
title: Arrange a collection of tuples in ascending order based on the second item (an integer)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The list of tuples can be sorted by using the sorted() function with the key parameter set to the itemgetter() function with an argument of 1.
---

**Contents**

[TOC]

#Section 1: Creating a List of Tuples

tuple_list = [('A', 3), ('B', 2), ('C', 1), ('D', 4)]

#Section 2: Sorting the List

tuple_list.sort(key=lambda x: x[1])

#Section 3: Printing the Sorted List

print(tuple_list)

#Section 4: Output

[('C', 1), ('B', 2), ('A', 3), ('D', 4)]
