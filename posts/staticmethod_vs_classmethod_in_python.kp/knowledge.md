---
title: What is the distinction between a static method and a class method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: A @staticmethod is a method that does not receive any additional arguments, whereas a @classmethod receives the class as the first argument.
---

**Contents**

[TOC]

### @staticmethod

A @staticmethod is a method that is bound to a class rather than its objects. It does not require a reference to the class instance. A @staticmethod can be called either on the class (such as C.f()) or on an instance (such as C().f()). The @staticmethod is a routine that does not operate on an instance or class, but on the parameters that are passed to it.

### @classmethod

A @classmethod is a method that is bound to a class rather than its objects. It is called on the class, not on an instance of the class. A @classmethod can access or modify class state that applies across all instances of the class. The @classmethod is a routine that is bound to the class and not the object of the class. It can modify class state that would apply across all the instances of the class. It is also a factory method for creating objects for different use cases.
