---
title: What is the reason that python's 'private' methods are not truly private?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Python`s `private` methods are not actually private because they can still be accessed and modified from outside the class.
---

**Contents**

[TOC]

# Definition
Private methods in Python are methods that are marked with a single leading underscore. These methods are intended to be inaccessible from outside of the class definition, meaning that they cannot be called directly from outside of the class.

# Reasons
1. Python does not have a concept of private methods, unlike other languages such as Java. The single leading underscore is merely a convention used to indicate that a method should not be called from outside the class.

2. The single leading underscore can easily be bypassed by using the double leading underscore syntax, which is used to create "name mangling" in Python. This allows the method to be accessed from outside the class, effectively bypassing the intended private access.

3. Python does not have a way to enforce the private access of methods, so it is up to the developer to ensure that the methods are not accessed from outside the class. This can be difficult to do in large projects, as it requires keeping track of all the methods that should be private.
