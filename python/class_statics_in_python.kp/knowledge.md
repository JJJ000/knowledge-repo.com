---
title: Static class variables and methods
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Class (static) variables and methods are variables and methods that are shared among all instances of a class and can be accessed directly from the class itself.
---

**Contents**

[TOC]

### Definition
Class variables are variables that are shared among all instances of a class. They are defined within the class definition, but outside of any of the class's methods. Class methods are methods that are bound to a class rather than its object. They don’t require an instance of a class to be used, and are usually used to create factory methods.

### Example
For example, consider the following class:

```python
class Circle:
    # Class Variable
    pi = 3.14
    
    # Constructor
    def __init__(self, radius):
        self.radius = radius
        
    # Instance Method
    def area(self):
        return self.radius * self.radius * Circle.pi
    
    # Class Method
    @classmethod
    def from_diameter(cls, diameter):
        return cls(diameter / 2)
```

In this example, `pi` is a class variable, and `from_diameter` is a class method.

### Usage
Class variables are useful for defining attributes and methods that are shared by all instances of a class. For example, the `pi` class variable defined in the example above is a useful value that can be shared by all instances of the `Circle` class.

Class methods can be used to create factory methods, which are methods that create and return instances of a class. In the example above, the `from_diameter` class method creates and returns an instance of the `Circle` class from a given diameter.
