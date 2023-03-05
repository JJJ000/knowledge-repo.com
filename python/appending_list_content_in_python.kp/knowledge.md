---
title: Add the items from one list to another list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To append the content of a list to another list in Python, use the extend() method.
---

**Contents**

[TOC]

# First, create the list variables

list1 = [1, 2, 3]
list2 = [4, 5, 6]

# Method 1 - Using the extend() method
# The extend() method adds every element of a list to the end of another list

list1.extend(list2)

print(list1)    # Output: [1, 2, 3, 4, 5, 6]


# Method 2 - Using the + operator
# The + operator concatenates two lists together

new_list = list1 + list2

print(new_list)    # Output: [1, 2, 3, 4, 5, 6]


# Method 3 - Using slicing and the += operator
# Slicing allows us to get a subset of a list
# The += operator is used to modify a list in place by adding another list to it

list1 += list2[:]

print(list1)    # Output: [1, 2, 3, 4, 5, 6]
