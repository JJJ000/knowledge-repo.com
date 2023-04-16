---
title: See if something is (not) present in a list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To check if something is (not) in a list in Python, use the `in` (or `not in`) operator.
---

**Contents**

[TOC]

**Using the 'in' Operator**

The simplest way to check if something is (not) in a list in Python is to use the 'in' operator. This operator will return a Boolean (True or False) value depending on whether or not the specified element is present in the list.

For example, if we have the list `my_list = [1, 2, 3]` and we want to check if the number 4 is in the list, we can use the following code:

`4 in my_list`

This will return False, since 4 is not in the list.

**Using the 'not in' Operator**

The 'not in' operator works similarly to the 'in' operator, but it returns True if the specified element is not in the list.

For example, if we have the same list as before, `my_list = [1, 2, 3]`, and we want to check if the number 4 is not in the list, we can use the following code:

`4 not in my_list`

This will return True, since 4 is not in the list.

**Using the index() Method**

Another way to check if something is (not) in a list in Python is to use the index() method. This method will return the index of the specified element in the list, or a ValueError if the element is not present.

For example, if we have the list `my_list = [1, 2, 3]` and we want to check if the number 4 is in the list, we can use the following code:

`my_list.index(4)`

This will return a ValueError, since 4 is not in the list.

**Using the count() Method**

The final way to check if something is (not) in a list in Python is to use the count() method. This method will return the number of occurrences of the specified element in the list.

For example, if we have the list `my_list = [1, 2, 3]` and we want to check if the number 4 is in the list, we can use the following code:

`my_list.count(4)`

This will return 0, since 4 is not in the list.
