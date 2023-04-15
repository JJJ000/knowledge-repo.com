---
title: What is the process of creating a class property?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To make a class property in Python, use the `@property` decorator above the method definition.
---

**Contents**

[TOC]

### Section 1: Defining a class

The first step in creating a class property is to define a class in Python. This can be done using the `class` keyword followed by the name of the class, which should start with a capital letter. For example, we can define a class called `Person` as follows:

```python
class Person:
    pass
```

This creates a simple empty class that doesn't do anything, but we can now add attributes and methods to it.

### Section 2: Adding a class property

To add a class property in Python, we can define a class attribute that is shared by all instances of the class. This can be done by defining a variable inside the class but outside of any method. For example, we can define a class attribute called `species` for the `Person` class as follows:

```python
class Person:
    species = 'human'
```

Now, all instances of the `Person` class will have a `species` attribute with the value `'human'`.

### Section 3: Accessing the class property

To access the class property from outside the class, we can use the dot notation to refer to it using the class name. For example, we can access the `species` property of the `Person` class as follows:

```python
print(Person.species)
```

This will output `'human'`.

### Section 4: Updating the class property

To update the class property, we can simply assign a new value to it using the class name. For example, to change the `species` attribute of the `Person` class to `'mammal'`, we can do the following:

```python
Person.species = 'mammal'
```

Now, all instances of the `Person` class will have a `species` attribute with the value `'mammal'`.
