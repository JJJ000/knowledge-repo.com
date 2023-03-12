---
title: The referenced local variable was not yet assigned
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: This error occurs when a variable is used before it has been assigned a value within a function or code block.
---

**Contents**

[TOC]

Introduction
--------------
In Python, variables can be either global or local. Global variables are defined outside of any function, whereas local variables are defined inside a function. In this article, we will discuss local variables and the issue of "local variable referenced before assignment" in Python.

What is a Local Variable?
------------------------------
A local variable is a variable that is declared inside a function. Local variables are only accessible within the function where they are defined, and cannot be used outside of the function. When a function is called, the local variables are created, and when the function terminates, the local variables are destroyed.

What is "Local variable referenced before assignment" in Python?
----------------------------------------------------------------------
In Python, if you attempt to use a local variable before it has been assigned a value, you will receive a "local variable referenced before assignment" error. This error occurs when you try to access the value of a local variable before it has been initialized or assigned a value. 

There are a few common reasons why this error occurs:
- The variable is defined in one branch of an if statement, and used in another branch
- The variable is defined inside a try block, and used outside of it
- The variable is defined inside a loop, and used outside of it

Conclusion
-----------
In conclusion, local variables in Python are only accessible within the function where they are defined. When you attempt to use a local variable before it has been initialized or assigned a value, you will receive a "local variable referenced before assignment" error. To avoid this error, ensure that all local variables are initialized before they are used, and that they are only used within the function where they are defined.
