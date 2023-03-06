---
title: Go through attributes of an object in Python using iteration
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can loop through the keys or values of an object using a for loop and the methods .keys() or .values().
---

**Contents**

[TOC]

## Introduction
Iterating over object attributes can be useful when you want to access or manipulate the data stored in an object. In Python, you can iterate over object attributes using a variety of techniques. In this article, we will cover four common ways to iterate over object attributes in Python.

## Using __dict__
The first method for iterating over object attributes in Python is to use the __dict__ attribute. Every Python object has a __dict__ attribute that contains all of the object's attributes as key-value pairs. You can iterate over these key-value pairs using a for loop.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
person = Person("Alice", 25)
for attr, value in person.__dict__.items():
    print(attr, "=", value)
```

In this example, we use the __dict__ attribute to loop over all the attributes of the Person object and print their values.

## Using dir()
Another way to iterate over object attributes in Python is to use the dir() function. The dir() function returns a list of all the attributes and methods of an object. You can then filter this list to only include attributes you are interested in, and loop over them using a for loop.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
person = Person("Alice", 25)
for attr in dir(person):
    if not callable(getattr(person, attr)) and not attr.startswith("__"):
        print(attr, "=", getattr(person, attr))
```

In this example, we use the dir() function to get a list of all the attributes of the Person object. We filter this list using the callable() and startswith() functions to exclude methods and private attributes, and then loop over the remaining attributes to print their values.

## Using vars()
A third way to iterate over object attributes in Python is to use the vars() function. The vars() function returns the __dict__ attribute of an object, so you can use it in a for loop to loop over all the attributes of an object.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
person = Person("Alice", 25)
for attr, value in vars(person).items():
    print(attr, "=", value)
```

In this example, we use the vars() function to get the __dict__ attribute of the Person object, and then loop over its key-value pairs to print the values of all the attributes.

## Using getattr()
Finally, you can use the built-in function getattr() to access object attributes dynamically. This can be useful if you need to access attributes based on user input or other runtime conditions. 

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
person = Person("Alice", 25)
attr_name = "name"
value = getattr(person, attr_name)
print(attr_name, "=", value)
```

In this example, we use the getattr() function to dynamically access the name attribute of the Person object based on the value of the attr_name variable. This can be useful if you need to access object attributes based on runtime conditions or user input.

## Conclusion
There are several ways to iterate over object attributes in Python, each with its strengths and weaknesses. By understanding these techniques, you can access and manipulate the data stored in objects more effectively, making it easier to write clean, efficient code.
