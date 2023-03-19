---
title: Using a custom type as a key for a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: An object of custom type can be used as a dictionary key in Python, as long as it is hashable and has properly defined `\_\_hash\_\_()` and `\_\_eq\_\_()` methods.
---

**Contents**

[TOC]

Section 1: Introduction to Dictionary Keys in Python
In Python, a dictionary is an unordered collection of key-value pairs, where each key should be unique. The keys in a dictionary should be of an immutable type such as a string, tuple, or int. A dictionary key can't be of a mutable type, such as a list or a dictionary.

Section 2: Custom Types as Dictionary Keys in Python
When it comes to custom types, we can use an immutable type to represent our custom type as a key in a dictionary. We can do this by defining a hash function for our custom type. A hash function returns an integer value, which will be used as the dictionary key. An important requirement for a hash function is that it should return the same value every time it's called with the same input value.

Section 3: Defining the Hash Function for Custom Types in Python
To define a hash function for a custom type, we'll need to implement two special methods in Python, __eq__() and __hash__(). The __eq__() method is used to compare two instances of our custom type, and the __hash__() method is used to generate a hash value for an instance. 

Section 4: Example Code for Using Custom Types as Dictionary Keys in Python
Here's an example code snippet that demonstrates how to use a custom type as a dictionary key in Python:

```python
class Person:
    def __init__(self, name):
        self.name = name

    def __eq__(self, other):
        return isinstance(other, Person) and self.name == other.name

    def __hash__(self):
        return hash(self.name)

people = {}
person1 = Person('Alice')
person2 = Person('Bob')
people[person1] = 1
people[person2] = 2
print(people[person1]) # Output: 1
print(people[person2]) # Output: 2
```

In this example, we defined a custom class Person and implemented the __eq__() and __hash__() methods. We then created two instances of Person and used them as keys in a dictionary. The dictionary correctly retrieves the values corresponding to each key, demonstrating that our custom type is working as a dictionary key in Python.
