---
title: Is it necessary to invoke the __init__() of the parent class in the __init__() method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Yes, it should, if the child class has a parent class and it needs to inherit its attributes and methods.
---

**Contents**

[TOC]

Introduction
In Python, when creating a class, it is essential to initialize the objects' attributes with appropriate values. The constructor or __init__() method is responsible for initializing these attributes. In some cases, we may want to call the parent class's constructor to initialize its attributes before adding new ones. This raises the question of whether we should call the parent class's __init__() method or not?

Yes, call the parent class's __init__()
When creating a subclass, it is usually a good idea to call the parent class's __init__() method explicitly. This ensures that the parent class's attributes are initialized before initializing the attributes specific to the subclass. We can do this by using the super() function to call the parent class's __init__() method. By doing this, we ensure the subclass is properly initialized with all its inherited attributes. Here is an example:

```
class Animal:
    def __init__(self, name):
        self.name = name
        print('Animal initialized')
        
class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)
        self.breed = breed
        print('Dog initialized')

d = Dog('Max', 'Labrador')
```

In the above example, we create two classes, Animal and Dog. The Dog class is a subclass of the Animal class. When initializing an object of the Dog class, we call the parent class's constructor using super() before initializing the breed attribute. This ensures that the name attribute from the Animal class is initialized before adding a new attribute.

No, don't call the parent class's __init__()
In some cases, we may not want to call the parent class's __init__() method. This happens when we don't need to initialize any of the parent class's attributes. In such situations, we can simply omit the call to the parent class's __init__() method. Here is an example:

```
class Animal:
    def __init__(self):
        print('Animal initialized')
        
class Dog(Animal):
    def __init__(self, breed):
        self.breed = breed
        print('Dog initialized')

d = Dog('Labrador')
```

In the above example, we create two classes, Animal and Dog. The Dog class is a subclass of the Animal class. When initializing an object of the Dog class, we don't need to initialize any attributes from the Animal class. Hence, we don't call the parent class's __init__() method.

It depends on the situation
In some cases, it may not be necessary to call the parent class's __init__() method. Similarly, in some cases, it may be necessary to call it explicitly. The decision to call or not to call the parent class's __init__() method depends entirely on the requirements of the subclass. If the subclass needs to initialize the parent class's attributes, it should call the parent class's __init__() method. If not, it should omit the call. 

Conclusion
In conclusion, whether to call the parent class's __init__() method or not depends on the requirements of the subclass. If the subclass needs to initialize the parent class's attributes, it should call the parent class's __init__() method. If not, it should omit the call. It is usually a good idea to call the parent class's __init__() method to ensure that the parent class's attributes are initialized before initializing the subclass's attributes. We can call the parent class's __init__() method using super().
