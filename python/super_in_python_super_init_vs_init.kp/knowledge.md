---
title: What is the distinction between using super().__init__() and explicitly calling the superclass __init__() method in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: In Python, the super() function allows a subclass to access methods and properties of its parent class, while explicitly calling the superclass`s \_\_init\_\_() method allows for customizing the subclass`s initialization.
---

**Contents**

[TOC]

#What is 'super'?

In Python, the super() builtin returns a proxy object (temporary object of the superclass) that allows us to access methods of the base class. It is used to gain access to inherited methods – from a parent or sibling class – that has been overwritten in a class object.

#Difference between super().__init__() and explicit superclass __init__()

The main difference between super().__init__() and explicit superclass __init__() is that the former does not require you to explicitly specify the name of the superclass. The super() function will automatically search the inheritance tree and call the __init__() method of the superclass.

On the other hand, when using explicit superclass __init__(), you must explicitly specify the name of the superclass in the call. This means that if the inheritance tree is changed, the call to the superclass __init__() must also be updated.

#Advantages of using super()

Using super() has several advantages over explicit superclass __init__() calls:

1. It is easier to maintain code when using super(), since the inheritance tree does not need to be explicitly specified.

2. It is more consistent, since the same call to super() will always call the same superclass __init__() method.

3. It is more efficient, since the super() call does not require an explicit search of the inheritance tree.

#Disadvantages of using super()

There are some disadvantages to using super() as well:

1. It can be difficult to debug, since the call to super() is not explicit.

2. It can lead to errors if the inheritance tree is changed and the call to super() is not updated.

3. It can lead to unexpected results if the superclass __init__() method is not called as expected.
