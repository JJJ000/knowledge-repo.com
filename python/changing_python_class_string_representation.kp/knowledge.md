---
title: What is the process of altering the textual representation of a Python class called?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Override the \_\_str\_\_ method.
---

**Contents**

[TOC]

## Introduction to Changing String Representation of a Python Class

Every class in Python has a string representation that is displayed when the object is printed, or when it is used in string operations like concatenation. By default, this representation is not very useful, as it simply displays the class name and the memory location of the object. However, it is possible to change the string representation of a class to make it more informative and useful.

## Section 1: Define `__str__` Method for the Class

The first step in changing the string representation of a class is to define the `__str__` method for the class. This method should return a string that represents the object in a way that is meaningful and useful. The string can contain any information that the programmer wants to include, such as the values of certain attributes, or a summary of the object's state.

## Section 2: Implement the `__repr__` Method

In addition to the `__str__` method, it is also useful to implement the `__repr__` method for the class. This method should return a string that represents the object in a way that is unambiguous and can be used to recreate the object. This is particularly useful for debugging purposes, as it allows the programmer to see exactly what the object looks like and how it is constructed.

## Section 3: Format the String Appropriately

When defining the `__str__` and `__repr__` methods, it is important to format the string appropriately, so that it is easy to read and understand. This may involve using line breaks, indentation, and other formatting options to make the string more readable. It is also important to consider the length of the string and whether it will be truncated in certain contexts, such as when displayed in a terminal window.

## Section 4: Example of Changing String Representation

Here is an example of how to change the string representation of a class:

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def __str__(self):
        return f"{self.year} {self.make} {self.model}"

    def __repr__(self):
        return f"Car('{self.make}', '{self.model}', {self.year})"

my_car = Car("Toyota", "Corolla", 2021)

print(my_car)  # "2021 Toyota Corolla"
```

In this example, the `Car` class has been defined with `__str__` and `__repr__` methods that return the make, model, and year of the car in a formatted string. When we create a new instance of the `Car` class and print it, we get a customized string representation that is more informative than the default representation.

## Conclusion

Changing the string representation of a class in Python is a useful technique for making objects easier to read and understand. By defining the `__str__` and `__repr__` methods for a class and formatting the string appropriately, it is possible to create a customized string representation that provides valuable information about the object.
