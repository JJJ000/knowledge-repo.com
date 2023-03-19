---
title: What steps can be taken to prevent instances from sharing class data?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use instance variables instead of class variables.
---

**Contents**

[TOC]

## Introduction
In Python, class data can be shared among instances which is known as class level data. This means that any changes made to the attribute value of one instance will be reflected on all instances. However, sometimes we might want to avoid this behavior and have instance-specific attributes. In this article, we will discuss some ways to avoid having class data shared among instances in Python.

## Create instance variables in the constructor
One way to avoid sharing class data among instances is to create instance variables in the constructor. This will ensure that each instance has its own instance variables and changes made to one instance will not affect the others. Here is an example:

```
class MyClass:
    def __init__(self, var):
        self.var = var

a = MyClass(1)
b = MyClass(2)
print(a.var) # Output: 1
print(b.var) # Output: 2
```

In this example, the `__init__` method is used to create an instance variable `var` for each instance. When we create `a` and `b`, we pass a value to the constructor which is assigned to the `var` attribute of each instance. As you can see in the output, the values of `a.var` and `b.var` are different, indicating that they are instance-specific.

## Use class methods instead of class variables
Another way to avoid having class data shared among instances is to use class methods instead of class variables. Class methods are methods that are bound to the class rather than to an instance. They can be used to create class-specific behavior that is not tied to the state of the instance. Here is an example:

```
class MyClass:
    @classmethod
    def my_method(cls):
        print("This is a class method")

MyClass.my_method() # Output: This is a class method
```

In this example, we define a class method `my_method` using the `@classmethod` decorator. This method does not take any instance-specific arguments and is bound to the class `MyClass`. We can call this method using the class name `MyClass.my_method()`. As you can see in the output, the method is executed without any instance-specific behavior.

## Use instance methods instead of class variables
Another way to avoid having class data shared among instances is to use instance methods instead of class variables. Instance methods are methods that are bound to the instance rather than to the class. They can be used to create behavior that is tied to the state of the instance. Here is an example:

```
class MyClass:
    def __init__(self, var):
        self.var = var

    def my_method(self):
        print("Value of var is:", self.var)

a = MyClass(1)
b = MyClass(2)
a.my_method() # Output: Value of var is: 1
b.my_method() # Output: Value of var is: 2
```

In this example, we define an instance method `my_method` that takes `self` as an argument, which refers to the instance. This method accesses the instance variable `var` and prints its value. When we create `a` and `b` and call the `my_method` method on each instance, we get different output, indicating that the behavior is instance specific.

## Conclusion
In this article, we discussed how to avoid having class data shared among instances in Python. We explored three different approaches: creating instance variables in the constructor, using class methods instead of class variables, and using instance methods instead of class variables. By using these techniques, we can create more flexible and maintainable code that better suits our needs.
