---
title: What is the purpose of calling __init__() after __new__()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Because \_\_new\_\_() creates a new object and \_\_init\_\_() initializes it.
---

**Contents**

[TOC]

#### __new__()
__new__() is a static method that is responsible for creating a new instance of a class. It is the first method called when creating an instance of a class and is usually used to initialize the instance before __init__() is called.

#### __init__()
__init__() is a method that is responsible for initializing an instance of a class. It is called after __new__() is called and is used to set up the instance variables and other attributes of the instance.

#### Why __init__() is Called After __new__()
The reason __init__() is called after __new__() is because __new__() creates the instance of the class and __init__() initializes it. This allows the instance to be initialized with the correct values before it is used. It also allows for more flexibility when creating instances of classes, as __new__() can be used to create different types of instances.
