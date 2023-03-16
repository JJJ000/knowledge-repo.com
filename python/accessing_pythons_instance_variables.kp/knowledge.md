---
title: What is the method for obtaining instance variables in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: To get an instance variable in Python, access it using the dot notation after the object name.
---

**Contents**

[TOC]

Getting Instance Variables in Python

An instance variable is a variable that belongs to an object, and every object created from the same class has its own unique set of instance variables. In Python, there are various ways to access instance variables of an object. Here, we will discuss some of the most commonly used methods to get instance variables in Python.

**1. Using dot notation**

The simplest and most direct way to access an instance variable is by using dot notation. To get the instance variable x of an object obj, we simply write:

`obj.x`

For example, let's say we have a class called Person with an instance variable called name:

```
class Person:
    
    def __init__(self, name):
        self.name = name
```

To get the name of a person object, we can use the dot notation as follows:

```
p = Person('John')
print(p.name)  # Output: John
```

**2. Using the getattr() function**

The getattr() function is a built-in Python function that allows us to retrieve the value of an instance variable by passing in the object and the name of the variable as strings. The syntax for using getattr() is:

`getattr(obj, 'var')`

For example, suppose we have a class called Student with instance variables called name and age:

```
class Student:
    
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

To get the age of a student object, we can use the getattr() function as follows:

```
s = Student('Alice', 20)
print(getattr(s, 'age'))  # Output: 20
```

**3. Using the vars() function**

The vars() function is another built-in function in Python that returns a dictionary containing all instance variables of an object. The syntax for using vars() is:

`vars(obj)`

For example, let's say we have a class called Car with instance variables called make and model:

```
class Car:
    
    def __init__(self, make, model):
        self.make = make
        self.model = model
```

To get all the instance variables of a car object, we can use the vars() function as follows:

```
c = Car('Toyota', 'Camry')
print(vars(c))  # Output: {'make': 'Toyota', 'model': 'Camry'}
```

**4. Using the __dict__ attribute**

Finally, we can also access instance variables by using the __dict__ attribute of an object. The __dict__ attribute is a dictionary that contains all the instance variables of an object. The syntax for using __dict__ is:

`obj.__dict__`

For example, let's say we have a class called Rectangle with instance variables called width and height:

```
class Rectangle:
    
    def __init__(self, width, height):
        self.width = width
        self.height = height
```

To get all the instance variables of a rectangle object, we can use the __dict__ attribute as follows:

```
r = Rectangle(10, 5)
print(r.__dict__)  # Output: {'width': 10, 'height': 5}
```

In conclusion, there are several ways to get instance variables in Python. We can use dot notation, the getattr() function, the vars() function, or the __dict__ attribute to retrieve the values of instance variables of an object.
