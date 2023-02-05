---
title: What is the best way to remove elements from a dictionary while looping through it?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can delete items from a dictionary while iterating over it in Python by using the del keyword.
---

**Contents**

[TOC]

# 1. Using the `pop()` Method
The `pop()` method can be used to delete items from a dictionary while iterating over it. This method takes the key of the item to be deleted as an argument. It removes the item from the dictionary and returns its value.

# 2. Using the `del` Statement
The `del` statement can also be used to delete items from a dictionary while iterating over it. This statement takes the key of the item to be deleted as an argument. It deletes the item from the dictionary without returning its value.

# 3. Iterating Through a Copy of the Dictionary
Another way to delete items from a dictionary while iterating over it is to iterate through a copy of the dictionary. This can be done using the `copy()` method. This method creates a shallow copy of the dictionary which can then be iterated over. The items can then be deleted from the original dictionary using the `pop()` or `del` methods.

# 4. Using a Dictionary Comprehension
A fourth way to delete items from a dictionary while iterating over it is to use a dictionary comprehension. This is a way of creating a new dictionary from an existing dictionary. The new dictionary can be created by filtering out the items that should be deleted. This can be done by using an `if` statement in the comprehension.
