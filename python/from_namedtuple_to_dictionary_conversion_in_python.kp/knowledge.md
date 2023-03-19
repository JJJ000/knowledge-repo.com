---
title: Transform a namedtuple into a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the \_asdict() method to convert a namedtuple into a dictionary in Python.
---

**Contents**

[TOC]

## Introduction
In Python, `namedtuple` is a subclass of a tuple object that enables the user to give names to each element in the tuple. Sometimes, it may be necessary to convert a `namedtuple` object into a dictionary. In this article, we will explore various methods of converting a namedtuple into a dictionary.

## Using _asdict()_ method
The easiest method of converting a `namedtuple` into a dictionary is by using the `asdict()` method. This method returns an `OrderedDict` object, which can be further converted into a dictionary. 

```python
from collections import namedtuple

# Creating a namedTuple and assigning values to it
Person = namedtuple('Person', ['name', 'age', 'gender'])
person_obj = Person('Alice', 26, 'Female')

# Converting namedtuple into dictionary
person_dict = dict(person_obj._asdict())

print(person_dict) # Output: {'name': 'Alice', 'age': 26, 'gender': 'Female'}
```

## Using _vars()_ function
Another method of converting a `namedtuple` object into a dictionary is by using the `vars()` function. This method returns the `__dict__` attribute of the `namedtuple` object.

```python
from collections import namedtuple

# Creating a namedTuple and assigning values to it
Car = namedtuple('Car', ['make', 'model', 'year'])
car_obj = Car('Honda', 'Civic', 2020)

# Converting namedtuple into dictionary
car_dict = vars(car_obj)

print(car_dict) # Output: {'make': 'Honda', 'model': 'Civic', 'year': 2020}
```

## Using _dict()_ constructor
Alternatively, we can also use the `dict()` constructor to convert a `namedtuple` object into a dictionary by passing the `_asdict()` method as an argument.

```python
from collections import namedtuple

# Creating a namedTuple and assigning values to it
Student = namedtuple('Student', ['name', 'age', 'major'])
student_obj = Student('Bob', 22, 'Computer Science')

# Converting namedtuple into dictionary
student_dict = dict(student_obj._asdict())

print(student_dict) # Output: {'name': 'Bob', 'age': 22, 'major': 'Computer Science'}
```

## Conclusion
In this article, we discussed three methods for converting a `namedtuple` into a dictionary. We can use any of the above methods depending on our use case and preferences. It is important to note that the `namedtuple` attributes must be valid Python identifiers for these methods to work properly.
