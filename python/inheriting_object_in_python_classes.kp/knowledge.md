---
title: What is the purpose of having Python classes inherit from the object class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Python classes inherit object in order to provide the basic functionality for all classes in Python.
---

**Contents**

[TOC]

# Introduction 
Python classes inherit from the object class by default. This means that all classes have access to the methods and attributes of the object class. 

# Benefits of Inheriting from Object
Inheriting from object provides a number of benefits for Python classes. Firstly, it allows classes to take advantage of the built-in methods and attributes of the object class. These methods and attributes provide a number of useful features, such as the ability to compare objects and to represent them as strings. 

Secondly, inheriting from object gives classes access to the special methods that are used to implement operators. These special methods, such as __add__ and __eq__, allow classes to define how they should behave when they are used with operators. 

# Drawbacks of Inheriting from Object
One of the drawbacks of inheriting from object is that it can lead to a large amount of code bloat. This is because the object class contains a large number of methods and attributes that classes may not need. As a result, classes can end up containing a large amount of code that they do not actually use. 

Another drawback of inheriting from object is that it can lead to unexpected behavior. This is because the methods and attributes of the object class can override the methods and attributes of the class that is inheriting from it. As a result, classes may end up behaving in unexpected ways. 

# Conclusion
In summary, Python classes inherit from object by default. This provides a number of benefits, such as access to built-in methods and attributes and the ability to define how classes should behave when used with operators. However, it can also lead to code bloat and unexpected behavior.
