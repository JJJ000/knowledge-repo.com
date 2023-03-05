---
title: What is the reason for Python lists having pop() but not push()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Python lists have pop() instead of push() because they follow a stack data structure where elements are added and removed from the top of the stack.
---

**Contents**

[TOC]

Python Lists Overview
---

In Python, a list is a data structure that is mutable, ordered, and allows duplicate elements. Mutable means that the list can be modified after its creation. 

Push() Method
---

The push() method is used to add an element to the end of an array or list. It is commonly used in other programming languages.

Pop() Method
---

The pop() method, available in Python lists, removes and returns the last element in the list. This method reduces the length of the list by one. 

Python's Approach
---

Python has chosen to not include a push() method in its lists, instead opting for the append() method. The append() method adds an element to the end of the list, and has the same behavior as push() would in other languages. Python's choice of method naming is influenced by its focus on readability and simplification. By using append() instead of push(), it makes the code easier for programmers to understand and makes it more consistent with the rest of the list's methods.
