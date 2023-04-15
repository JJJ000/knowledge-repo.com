---
title: What is the procedure to obtain or modify an object attribute if provided with a string matching its name?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To access object attribute given string corresponding to the name of that attribute in Python, use the built-in function `getattr(object, attribute\_name)` to get the attribute value or `setattr(object, attribute\_name, value)` to set the attribute value.
---

**Contents**

[TOC]

# Introduction
In Python, accessing object attributes using their string names involves the use of a built-in function called `getattr()`. This function allows you to retrieve the value of an attribute associated with an object using the attribute's name as a string. Similarly, the `setattr()` function is used to set the value of an attribute using its string name. In this guide, we will outline the steps required to access object attributes in Python using their string names.


## Accessing Object Attributes using getattr() function

To access object attributes using the `getattr()` function, you need to follow these steps:

1. First, you need to define your object.
2. Next, you need to pass the object and the name of the attribute you want to access as a string to the `getattr()` function.
3. Finally, the `getattr()` function will return the value of the attribute you want to access. 

Here's an example:

```python
class Person:
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

person = Person("John", 25, "Male")

# Accessing "name" attribute
name = getattr(person, "name")
print(name) # Output: John

# Accessing "age" attribute
age = getattr(person, "age")
print(age) # Output: 25
```


## Setting Object Attributes using setattr() function

To set object attributes using the `setattr()` function, you need to follow these steps:

1. First, you need to define your object.
2. Next, you need to pass the object, the name of the attribute you want to set as a string, and the new value to the `setattr()` function.
3. Finally, the `setattr()` function will set the new value to the attribute you want to update.

Here's an example:

```python
class Person:
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

person = Person("John", 25, "Male")

# Setting "name" attribute
setattr(person, "name", "James")
print(person.name) # Output: James

# Setting "age" attribute
setattr(person, "age", 30)
print(person.age) # Output: 30
```


## Handling Exceptions while Accessing or Setting Object Attributes

In some cases, the attribute you want to access or set may not exist in the object. In such scenarios, you can use try-except blocks to handle the exceptions.

For instance, let's say you want to access or set an attribute named "salary" that doesn't exist in the object. Here's an example:

```python
class Person:
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

person = Person("John", 25, "Male")

# Handling AttributeError exception while accessing "salary" attribute
try:
    salary = getattr(person, "salary")
    print(salary)
except AttributeError:
    print("The 'salary' attribute does not exist in the Person object.")

# Handling AttributeError exception while setting "salary" attribute
try:
    setattr(person, "salary", 50000)
except AttributeError:
    print("The 'salary' attribute does not exist in the Person object.")
```

Output: 
```
The 'salary' attribute does not exist in the Person object.
The 'salary' attribute does not exist in the Person object.
```

## Conclusion

In this guide, we covered the steps required to access or set object attributes in Python using their string names. We used the `getattr()` and `setattr()` functions to perform these operations while also showing how to handle exceptions in scenarios where the object attribute doesn't exist.
