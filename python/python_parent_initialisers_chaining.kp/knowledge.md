---
title: Restructuring the title python's process of calling parent initializers in a chain
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: In Python, you can chain-call parent initializers by using the super() function inside the child class`s initializer method.
---

**Contents**

[TOC]

Introduction:

Python allows for class inheritance, where a child class can inherit methods and variables from a parent class. In order to properly initialise a child object, the parent object's initialiser must also be called, which can be done using super(). This function can be used to call methods from the parent class, including the initialiser. 

Getting started:

To understand how to use super() to chain-call parent initializers, we must first understand the inheritance hierarchy. A child class inherits from a parent class, which can also inherit from another parent class. Thus, there is a chain of inheritance that must be followed when calling parent initialisers. 

Calling Parent Initialisers with super():

To call the initialiser of a parent class, we simply use super() in the child class initialiser. super() takes two arguments - the child class name and self, which refers to the instance of the child class. Once called, super() returns a temporary object of the superclass, allowing us to call its methods. To call the superclass initialiser, we pass in the arguments from the child class initialiser. This will call the initialiser from the first parent class, and then continue calling each parent's initialiser until it reaches the object class. 

Example:

```
class Parent:
    def __init__(self, name):
        self.name = name

class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

child = Child("John", 10)
print(child.name)
print(child.age)
```

Output:
```
John
10
```

Conclusion:

When using inheritance in Python, it's essential to call parent initialisers to ensure that the child object is properly initialised. We can do this by using the super() function in the child class initialiser, allowing us to call the initialiser of each parent class in the correct order. By following this pattern, we can ensure that our child objects have access to all the necessary variables and methods from its parent classes.
