---
title: Describing the purpose of python's '__enter__' and '__exit__'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The \_\_enter\_\_ and \_\_exit\_\_ methods are used in Python to create and manage context managers.
---

**Contents**

[TOC]

### What is Python's '__enter__' and '__exit__'?

Python's '__enter__' and '__exit__' are special methods that are defined within a class. They are used to create context managers, which are used to manage resources within a program.

### What does '__enter__' do?

The '__enter__' method is called when a context manager is entered. It is responsible for setting up the resources that will be used within the context manager. It is also responsible for returning an object that will be used within the context manager.

### What does '__exit__' do?

The '__exit__' method is called when a context manager is exited. It is responsible for cleaning up the resources that were set up by the '__enter__' method. It is also responsible for handling any exceptions that may have occurred while within the context manager.

### How are '__enter__' and '__exit__' used?

'__enter__' and '__exit__' are used together to create context managers. They are used to manage resources within a program, such as opening and closing files, setting up and tearing down databases, and so on. They are also used to handle any exceptions that may occur within the context manager.
