---
title: What are the differences between @classmethod and @staticmethod for a beginner?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @classmethod is a method that takes the class as the first argument, while @staticmethod is a method that does not take any additional arguments.
---

**Contents**

[TOC]

# @classmethod
A class method is a method that is bound to a class rather than its object. It doesn't require creation of a class instance, much like staticmethod. The difference between a static method and a class method is:

- A class method can access or modify class state while a static method can’t access or modify it.
- A class method takes cls as first parameter while a static method doesn’t take any parameter.

# @staticmethod
A static method is a method that is bound to a class rather than its object. It doesn’t require creation of a class instance, much like a class method. The difference between a static method and a class method is:

- A static method can't access or modify class state while a class method can access or modify it.
- A static method doesn't take any parameter while a class method takes cls as first parameter.

# Usage
Class methods are used to define methods that can be accessed by all instances of the class. They are also used to create factory methods, which are methods that create and return an instance of a class.

Static methods are used to define methods that belong to a class, but don't require access to the class or its instance data. They are also used to create utility functions that don't need access to the class or its instance data.
