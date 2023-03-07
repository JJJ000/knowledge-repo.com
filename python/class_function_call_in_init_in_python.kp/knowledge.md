---
title: Invoking a method of a class within the __init__ function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Yes, you can call a class function inside of \_\_init\_\_ in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, you can define a class with one or more functions, which are sometimes also referred to as class methods. These functions can be called from within the class as well as from outside of it. One special function in Python is the __init__ function, which is executed when a new instance of the class is created. In this article, we will explore whether it is possible to call a class function inside of __init__.

Section 2: Calling a Class Function from __init__
Yes, it is possible to call a class function from inside of __init__. In fact, it is quite common to do so. One reason to call a class function from __init__ is to initialize some object properties based on some other values or calculations. For example, suppose we have a class that represents a rectangle, and we want to initialize its properties height and width based on some other values. We can define a class function called calculate_area that does this calculation and then call it from __init__ as shown below:

```
class Rectangle:
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth
        self.area = self.calculate_area()
    
    def calculate_area(self):
        return self.length * self.breadth
```

In this example, we defined a __init__ function that takes two arguments length and breadth and initializes two object properties with the same name. Then we defined a class function called calculate_area that simply multiplies these two values and returns the result. Finally, we call this function from __init__ and assign its result to a new object property called area.

Section 3: Benefits of Calling a Class Function from __init__
As we can see from the above example, calling a class function from __init__ can be quite useful for initializing object properties based on some other values or calculations. This can help to simplify the code and improve its readability. Moreover, by defining the calculation in a separate function, we can reuse it elsewhere in our code if needed. For instance, suppose we wanted to calculate the area of a rectangle again later in the program. Instead of writing the same calculation again, we can simply call the calculate_area function.

Section 4: Conclusion
In summary, it is certainly possible to call a class function inside of __init__ in Python. In fact, this is quite common and can help to simplify the code, improve its readability, and facilitate code reuse. By defining calculations in separate functions, we can create more modular and organized code that is easier to maintain and debug.
