---
title: What is the appropriate usage of super with respect to argument passing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: The correct way to use super for argument passing in Python is by calling the parent class method with super() within the child class method and passing the required arguments for the parent class method.
---

**Contents**

[TOC]

Section 1: Introduction to super()

super() is a built-in function in Python that is mainly used to access inherited methods from a parent class. In Python, a subclass can inherit from a superclass, which means it can inherit instance variables, methods, and other attributes. The use of super() in Python is to call the corresponding method in the parent class.

Section 2: The correct way to use super()

To use super() properly in Python, the following steps should be followed:

1. First, call the superclass’s constructor method using super(). This helps to initialize the inherited instance variables.

2. Pass in the current class and self as arguments to the super() method. This helps super() to know the instance to work on.

3. Call the method in the parent class with the arguments needed by the method.

For example, let’s assume we have a class called SuperClass that has a method called class_method, and a subclass called SubClass. Here's how we can use super() in SubClass to inherit class_method from SuperClass:

```
class SuperClass:
    def class_method(self, arg1, arg2):
        # method implementation

class SubClass(SuperClass):
    def class_method(self, arg1, arg2, arg3):
        super(SubClass, self).class_method(arg1, arg2) # calling SuperClass method
        # method implementation
```

In this example, we call the superclass constructor method using super(), pass in SubClass and self as arguments to super(), and then call the class_method in the parent class with the necessary arguments.

Section 3: Passing arguments to super()

When passing arguments to super(), you need to pass in the current class and self as the first two arguments, followed by any other required arguments for the parent class. The arguments that you pass to super() are used by super() to find the correct method in the parent class to call.

For example:

```
class SuperClass:
    def __init__(self, arg1, arg2):
        # constructor implementation

class SubClass(SuperClass):
    def __init__(self, arg1, arg2, arg3):
        super(SubClass, self).__init__(arg1, arg2) # calling SuperClass constructor
        # constructor implementation
```

In this example, we pass in SubClass and self as the first two arguments, and arg1 and arg2 as the next two arguments, which are the required arguments in the constructor of the parent class (SuperClass).

Section 4: Conclusion

In conclusion, super() is a powerful built-in function in Python that allows inheritance of methods and other attributes from parent classes. Using super() properly involves calling the superclass constructor method, passing in the current class and self, and calling the parent method with the necessary arguments. By following these steps, you can use super() effectively to implement inheritance in your Python programs.
