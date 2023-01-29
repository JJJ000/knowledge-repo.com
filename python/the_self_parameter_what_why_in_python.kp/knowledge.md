---
title: What does the "self" parameter do? why is it necessary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `self` parameter is used to refer to the current instance of a class and is needed in Python to access instance attributes and methods.
---

**Contents**

[TOC]

#### What is self?
The `self` parameter is a reference to the current instance of a class. It is used to access the attributes and methods of a class from within the class itself.

#### Why is it needed in Python?
Python is an object-oriented language, which means that it uses classes to manage data and methods that can be used to manipulate that data. The `self` parameter is used to access the attributes and methods of the class from within the class itself. This allows the class to maintain its own internal state and manage its own data without relying on external variables.

#### How it works
When an instance of a class is created, the `self` parameter is automatically passed to the class constructor as the first argument. This allows the class to access its own attributes and methods from within the class. For example, if a class has an attribute called `name`, it can access this attribute by using `self.name`.

#### Conclusion
The `self` parameter is an essential part of Python's object-oriented programming model. It enables classes to maintain their own internal state and manage their own data without relying on external variables.
