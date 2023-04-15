---
title: What is the way to verify during runtime if a class is a subclass of another?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the built-in function issubclass() to check if one class is a subclass of another.
---

**Contents**

[TOC]

### Use the `issubclass()` Built-In Function
The easiest and most straightforward way to check if one class is a subclass of another is by using Python's built-in `issubclass()` function. This function takes two arguments: the first is the supposed subclass and the second is the supposed superclass. It returns `True` if the first argument is indeed a subclass of the second, and `False` otherwise.

Here's an example:


```python
class Vehicle:
    pass

class Car(Vehicle):
    pass

class Motorcycle(Vehicle):
    pass

print(issubclass(Car, Vehicle)) # True
print(issubclass(Motorcycle, Vehicle)) # True
print(issubclass(Car, Motorcycle)) # False
```

In this example, we have two subclasses: `Car` and `Motorcycle`. Both classes inherit from the `Vehicle` class, which is the superclass. We use the `issubclass()` function to check if `Car` and `Motorcycle` are indeed subclasses of `Vehicle`.


### Check the `__bases__` Attribute
Another way to check if one class is a subclass of another is by inspecting the `__bases__` attribute of the supposed subclass. This attribute is a tuple that contains the classes from which the subclass inherits.

Here's an example:


```python
class Animal:
    pass

class Dog(Animal):
    pass

class Cat(Animal):
    pass

print(Dog.__bases__) # (<class '__main__.Animal'>,)
print(Cat.__bases__) # (<class '__main__.Animal'>,)
```

In this example, we have two subclasses: `Dog` and `Cat`. Both classes inherit from the `Animal` class, which is the superclass. We can check if `Dog` is a subclass of `Animal` by inspecting the `__bases__` attribute of the `Dog` class.


### Use the `type()` Built-In Function
The `type()` function can be used to check if one class is a subclass of another. This function takes an object as its argument and returns its type. We can then use the `issubclass()` function to check if the returned type is a subclass of the supposed superclass.

Here's an example:


```python
class Shape:
    pass

class Rectangle(Shape):
    pass

r = Rectangle()

print(type(r)) # <class '__main__.Rectangle'>
print(issubclass(type(r), Shape)) # True
```

In this example, we have a subclass `Rectangle` that inherits from the `Shape` superclass. We create an instance of the `Rectangle` class and check its type using the `type()` function. We then use the `issubclass()` function to check if the type of `r` is a subclass of `Shape`.


### Check if an Instance Is an Instance of a Class
A final way to check if one class is a subclass of another is by checking if an instance of the supposed subclass is an instance of the supposed superclass. This method is less reliable than the others because an instance of a subclass may also be an instance of its superclass.

Here's an example:


```python
class Fruit:
    pass

class Apple(Fruit):
    pass

class Banana(Fruit):
    pass

a = Apple()
b = Banana()

print(isinstance(a, Fruit)) # True
print(isinstance(b, Fruit)) # True
```

In this example, we have two subclasses: `Apple` and `Banana`. Both classes inherit from the `Fruit` class, which is the superclass. We create instances of the `Apple` and `Banana` classes and check if they are instances of the `Fruit` class.
