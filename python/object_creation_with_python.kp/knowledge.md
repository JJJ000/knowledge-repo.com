---
title: The process of generating objects using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To create an object in Python, first define a class (which serves as a blueprint for the object) and then use the class to create an instance of the object using the syntax name\_of\_object = ClassName().
---

**Contents**

[TOC]

Creating Objects in Python

## Object-Oriented Programming in Python

Python is an object-oriented programming language that supports the creation and manipulation of objects. An object is an instance of a class, and a class is a blueprint for creating objects. 

## Defining Classes

To create an object in Python, you first need to define a class. A class is defined using the `class` keyword, followed by the class name and a colon. You can define variables and methods inside the class. 

```Python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def say_hello(self):
        print(f"Hello, my name is {self.name} and I'm {self.age} years old.")
```

In the above example, we have defined a class named `Person` with two variables `name` and `age` and a method `say_hello()`. The `__init__()` method is a special method that gets called when an object of the class is created. 

## Creating Objects

Once you have defined a class, you can create objects of that class using the class name and passing the required arguments to the `__init__()` method. 

```Python
person1 = Person("John", 30)
person2 = Person("Jane", 25)
```

In the above example, we have created two objects `person1` and `person2` of the `Person` class, with different values for the `name` and `age` variables. 

## Accessing Object Attributes

You can access the attributes of an object by using the dot notation. 

```Python
print(person1.name)  # Output: John
print(person2.age)   # Output: 25
```

In the above example, we are accessing the `name` attribute of `person1` and the `age` attribute of `person2`. 

## Conclusion

Creating objects in Python is easy. You can define a class, create objects of that class, and access the attributes of those objects using the dot notation. Python's object-oriented programming features make it a popular language for building complex applications.
