---
title: In python, what's the way to assign class attributes using keyword arguments (kwargs) arguments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can set class attributes from variable arguments using the setattr function in a class method that has **kwargs as a parameter.
---

**Contents**

[TOC]

# Introduction
In Python, you can use the double asterisk notation (`**`) to pass a variable-length dictionary of keyword arguments (kwargs) to a function or constructor. This can be especially useful when you need to set attributes for an object but don't want to hardcode them in advance. In this article, we'll explore how to use variable arguments to set class attributes in Python.

# Creating a Class with Default Attributes
First, let's create a basic class with some default attributes. We'll call it `Person` and give it `name`, `age`, and `height` attributes:

```python
class Person:
    def __init__(self, name='John', age=30, height=180):
        self.name = name
        self.age = age
        self.height = height
```

# Using Variable Arguments to Set Attributes
Now, let's modify the `Person` class to accept variable arguments. We can use the double asterisk notation (`**kwargs`) to capture any keyword arguments that are passed in:

```python
class Person:
    def __init__(self, name='John', age=30, height=180, **kwargs):
        self.name = name
        self.age = age
        self.height = height
        for key, value in kwargs.items():
            setattr(self, key, value)
```

What's happening here is that we're first setting the default attributes (`name`, `age`, and `height`) just as we did before. Then, we're iterating over any additional keyword arguments that were passed in and using the `setattr` function to set them as attributes on the `Person` object.

# Using the Class with Variable Arguments
Now that we've defined our `Person` class with support for variable arguments, let's see how we can use it. Here's an example:

```python
p1 = Person(name='Alice', age=25, height=170, occupation='teacher', country='USA')
print(p1.name) # Alice
print(p1.occupation) # teacher
print(p1.country) # USA
```

In this example, we're creating a new `Person` object called `p1` with some custom attributes (`occupation` and `country`) in addition to the default ones. We can see that the attributes are being set correctly by printing them out using dot notation.

# Conclusion
Using variable arguments is a powerful way to set class attributes in Python without hardcoding them in advance. By using the double asterisk notation (`**kwargs`) and the `setattr` function, you can make your classes more flexible and adaptable to changing requirements.
