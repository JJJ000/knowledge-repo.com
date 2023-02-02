---
title: What is the syntax for retrieving the last item in a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the [-1] index to access the last item of a list in Python.
---

**Contents**

[TOC]

### Using Slicing
Slicing is a powerful feature of Python that allows us to access parts of a list. We can use slicing to get the last items of a list. To do this, we use the syntax `list[start:stop:step]` where `start` is the index of the first item we want to include, `stop` is the index of the item we want to stop at (but not include), and `step` is the number of items we want to skip over.

For example, if we wanted to get the last three items of a list called `my_list`, we would use the syntax `my_list[-3:]`. This means that we want to start at the third item from the end (indicated by the negative index) and go to the end of the list.

### Using List Methods
Python also provides a number of list methods that can be used to access the last items of a list. The `pop()` method removes the last item from a list and returns it. This is useful if we want to get the last item without modifying the list.

The `pop()` method can also be used to get multiple items from the end of a list. For example, if we wanted to get the last three items from `my_list`, we could use the syntax `my_list[-3:].pop()` which would remove the last three items from the list and return them as a list.

### Using List Comprehension
List comprehension is a powerful feature of Python that allows us to create new lists from existing ones. We can use list comprehension to get the last items of a list by creating a new list that contains only the last items.

For example, if we wanted to get the last three items of `my_list`, we could use the syntax `[item for item in my_list[-3:]]`. This would create a new list containing only the last three items of `my_list`.

### Using Reverse
The `reverse()` method can be used to reverse a list so that the last items become the first items. We can then use slicing to get the last items of the reversed list. For example, if we wanted to get the last three items of `my_list`, we could use the syntax `my_list.reverse()[:3]`. This would reverse the list and then return the first three items.
