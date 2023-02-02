---
title: What is the process for creating multiple versions of the __init__ method based on the type of argument provided?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the isinstance() function to check the type of the argument passed to the \_\_init\_\_ method and call a different \_\_init\_\_ method based on the argument type.
---

**Contents**

[TOC]

#Section 1: Definition of Overloading
Overloading is a feature in Python that allows multiple functions to have the same name, but with different parameters. This is known as function overloading. The same concept can be applied to classes and their methods. When this happens, it is known as method overloading. 

#Section 2: Overloading the __init__ Method
The __init__ method is the constructor of a class and is called when an instance of a class is created. It can be overloaded by creating multiple __init__ methods with different parameters. 

#Section 3: Overloading Based on Argument Type
When overloading the __init__ method, the parameters can be of different types. For example, one __init__ method could take in two integers and the other could take in two strings. This allows for different initialization depending on the type of the arguments. 

#Section 4: Example
Below is an example of overloading the __init__ method based on argument type. 

```python
class Example:
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def __init__(self, x, y):
        self.x = int(x)
        self.y = int(y)

example1 = Example(1, 2)
example2 = Example("1", "2")
```
In this example, the first __init__ method takes in two integers and the second takes in two strings. Depending on the type of the arguments, a different __init__ method will be called.
