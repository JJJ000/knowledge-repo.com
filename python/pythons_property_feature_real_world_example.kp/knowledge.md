---
title: Can you provide a practical instance of how to utilize the property feature in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: One example is using the property feature to enforce constraints on the values of instance variables in a class.
---

**Contents**

[TOC]

1. Introduction
In Python, properties are a feature that allows us to access and modify an object's attributes by calling getter and setter methods. Properties are very useful when we want to encapsulate certain aspects of an object and control how they are accessed or modified. In this article, we will discuss a real-world example of how to use property features in Python.

2. Example
Suppose we have a class called Employee, which represents an employee in a company. The Employee class has attributes such as name, id, and salary. We want to set some rules on how to access and modify the salary attribute. We want to make sure that the salary is always a positive number, and we also want to keep track of how many times the salary was modified.

To achieve this, we can use the property feature of Python. We will create a private attribute called _salary, and we will define getter and setter methods for the salary attribute. In the getter method, we will return the value of _salary, and in the setter method, we will check if the new salary value is positive. If it is, we will set _salary to the new value and increment a counter called modifications. If the new salary value is not positive, we will raise an exception.

Here's the implementation of the Employee class with the property feature:

```python
class Employee:
    def __init__(self, name, id, salary):
        self.name = name
        self.id = id
        self._salary = salary
        self.modifications = 0
    
    @property
    def salary(self):
        return self._salary
    
    @salary.setter
    def salary(self, value):
        if value >= 0:
            self._salary = value
            self.modifications += 1
        else:
            raise ValueError("Salary should be a positive number")
```

With this implementation, we can create instances of the Employee class and access and modify their salary attribute using the usual dot notation. However, behind the scenes, the getter and setter methods are being called.

```python
# create an Employee instance
emp = Employee("John", 1234, 50000)

# access the salary attribute
print(emp.salary)  # output: 50000

# modify the salary attribute
emp.salary = 55000
print(emp.salary)  # output: 55000
print(emp.modifications)  # output: 1

# try to set a negative salary value
emp.salary = -1000
# raises a ValueError: Salary should be a positive number
```

3. Conclusion
The property feature of Python is a powerful tool that we can use to encapsulate and control how an object's attributes are accessed and modified. In the example we discussed above, we used the property feature to ensure that the salary attribute of the Employee class is always a positive number, and we also kept track of how many times the attribute was modified. With properties, we can create more robust and maintainable code that follows good object-oriented design principles.
