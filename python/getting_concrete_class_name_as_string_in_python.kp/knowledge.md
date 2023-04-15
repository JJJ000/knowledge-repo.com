---
title: What is the method to obtain the string representation of the concrete class name?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `\_\_class\_\_.\_\_name\_\_` attribute to get the concrete class name as a string in Python.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, we can access the class name of an object by using the built-in function `type()`. However, this function returns a type object, not a string. Therefore, we need to convert it to a string to use it in other operations or in our code. In this tutorial, we will discuss how to get the concrete class name as a string in Python.

Section 2: Using __class__.__name__

One way to get the class name as a string is by using the `__class__.__name__` attribute. This attribute returns the name of the class of an object as a string. Here's an example:

```python
class Person:
    def __init__(self, name):
        self.name = name
        
p = Person("John")
print(p.__class__.__name__)  # Output: "Person"
```
In the above example, we define a class `Person` with a constructor method that takes a name argument. Then, we create an object `p` of the `Person` class and print the class name of `p` using the `__class__.__name__` attribute.

Section 3: Using type() and str()

Another way to get the class name as a string is by using the `type()` function and the `str()` function to convert the type object to a string. Here's an example:

```python
class Animal:
    def __init__(self, species):
        self.species = species
        
a = Animal("Dog")
print(str(type(a)).split(".")[-1][:-2])  # Output: "Animal"
```

In the above example, we define a class `Animal` with a constructor method that takes a species argument. Then, we create an object `a` of the `Animal` class and print the class name of `a` by passing `type(a)` to the `str()` function. We then split the resulting string by "." and take the last element, which is the class name with a suffix of "\'>". Finally, we remove the suffix using slice notation.

Section 4: Conclusion

In this tutorial, we discussed two ways to get the concrete class name as a string in Python. The first way is by using the `__class__.__name__` attribute, and the second way is by using the `type()` function and the `str()` function. Both methods are valid and efficient, and it depends on personal preference which one to use.
