---
title: Sort a Python list in reverse order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To sort a list in descending order, use the list.sort(reverse=True) method.
---

**Contents**

[TOC]

# Section 1: Using the Sorted Function

The sorted() function can be used to sort a list in descending order. To do this, the reverse parameter must be set to True.

Example:

my_list = [3, 5, 1, 4, 2]

sorted_list = sorted(my_list, reverse=True)

print(sorted_list)

Output: [5, 4, 3, 2, 1]

# Section 2: Using the Sort Method

The list.sort() method can be used to sort a list in descending order. To do this, the reverse parameter must be set to True.

Example:

my_list = [3, 5, 1, 4, 2]

my_list.sort(reverse=True)

print(my_list)

Output: [5, 4, 3, 2, 1]

# Section 3: Using the Reversed Function

The reversed() function can be used to sort a list in descending order.

Example:

my_list = [3, 5, 1, 4, 2]

reversed_list = list(reversed(my_list))

print(reversed_list)

Output: [2, 4, 1, 5, 3]

# Section 4: Using the Reverse Method

The list.reverse() method can be used to sort a list in descending order.

Example:

my_list = [3, 5, 1, 4, 2]

my_list.reverse()

print(my_list)

Output: [2, 4, 1, 5, 3]
