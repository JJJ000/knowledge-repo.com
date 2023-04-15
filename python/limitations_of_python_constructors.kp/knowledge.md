---
title: Can't we define multiple constructors in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: False, it is possible to define multiple constructors using the `\_\_init\_\_` method with default parameter values or using the `@classmethod` decorator.
---

**Contents**

[TOC]

Yes, it is possible to define multiple constructors in Python. Here are four sections explaining how:

## 1. Understanding Constructors in Python

In Python, a constructor is a special method that is automatically invoked when an object is instantiated. It initializes the object's properties and sets the default values for its attributes. The __init__() method is the constructor method of a class, and it is called when an object of a class is created.

## 2. Defining Multiple Constructors using Polymorphism

In Python, it is possible to define multiple constructors for a class using polymorphism. Polymorphism is the ability of an object to take on many forms. In Python, this can be achieved by defining multiple __init__() methods in a class.

For example, let's say we have a class called Person that takes in two parameters - name and age. We can define multiple constructors in this class by using the concept of polymorphism.

```
class Person:
    def __init__(self, name=None, age=None):
        self.name = name
        self.age = age

    def __init__(self, name):
        self.name = name

    def __init__(self, age):
        self.age = age
```

Here, we have defined three constructors for the Person class. The first constructor takes in two parameters - name and age. The second constructor takes in only the name parameter, and the third constructor takes in only the age parameter.

When creating an object of the Person class, the appropriate constructor is chosen based on the number and type of parameters passed.

```
person1 = Person("Bob", 30)  # calls the first constructor
person2 = Person("Bob")      # calls the second constructor
person3 = Person(30)         # calls the third constructor
```

## 3. Using Default Arguments to Create Multiple Constructors

Another way to define multiple constructors in Python is by using default arguments. Default arguments are values that are assigned to function parameters if no argument value is passed.

```
class Person:
    def __init__(self, name=None, age=None):
        self.name = name
        self.age = age

    def __init__(self, name):
        self.__init__(name, None)

    def __init__(self, age):
        self.__init__(None, age)
```

Here, we have defined three constructors for the Person class again. The only difference is that we are using default arguments to create the constructors. When creating an object of the Person class, the appropriate constructor is chosen based on the number and type of arguments passed.

```
person1 = Person("Bob", 30)  # calls the first constructor
person2 = Person("Bob")      # calls the second constructor
person3 = Person(30)         # calls the third constructor
```

## 4. Conclusion

In conclusion, it is possible to define multiple constructors in Python. We can use polymorphism or default arguments to achieve this. However, it is important to note that if we define multiple constructors for a class, we should ensure that they do not have the same number and type of parameters, as this will result in a TypeError.
