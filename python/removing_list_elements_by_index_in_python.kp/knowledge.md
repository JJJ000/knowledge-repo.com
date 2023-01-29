---
title: How to delete an item from a list using its position
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To remove an element from a list by index in Python, use the del statement.
---

**Contents**

[TOC]

#1 Find the Index of the Element

The first step is to find the index of the element that needs to be removed. This can be done by using the index() method. The index() method searches for the given element in the list and returns its index.

#2 Remove the Element

Once the index of the element is found, it can be removed from the list using the del statement. The syntax for the del statement is del list_name[index].

#3 Confirm the Removal

To confirm that the element has been removed, the list can be printed out. This can be done using the print() function. The syntax for the print() function is print(list_name).

#4 Check for Success

The last step is to check that the element has been successfully removed. This can be done by using the in operator. The syntax for the in operator is element in list_name. If the element is not present in the list, then it has been successfully removed.
