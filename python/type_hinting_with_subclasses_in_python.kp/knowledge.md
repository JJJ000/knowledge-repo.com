---
title: Reformulation 'a subset classification within the type hinting system'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Subclass in type hinting in Python is indicated by using the syntax of `SubClassName` instead of `Any` as the data type hint.
---

**Contents**

[TOC]

# Introduction
Type hinting in Python is a way to specify the expected data types of function arguments and return values. This helps to catch errors early and make code more reliable. In addition to built-in types like int and str, Python allows users to define their own types, including subclasses. This guide will explain how to use subclassing in type hinting.

# Defining a subclass
Before using a subclass in type hinting, you must first define it. This is done using the class keyword, followed by the name of the subclass and the name of its parent class (also known as its superclass). For example, to define a subclass called MyString that inherits from the built-in str class:

```python
class MyString(str):
    pass
```

This creates a new class that behaves exactly like the str class, but with the ability to add new methods or attributes.

# Using a subclass in type hinting
Once you have defined a subclass, you can use it in type hinting. For example, imagine you have a function that takes a string argument and returns a new string with some modification. To specify that the argument must be an instance of MyString, you can add a type hint like this:

```python
def modify_string(s: MyString) -> MyString:
    # code here
    return MyString(result)
```

This tells users of the function that they must pass an instance of MyString, not just any str.

# Polymorphism with subclassing
One of the benefits of subclassing is that it allows for polymorphic behavior. This means that functions can accept objects of different subclasses, as long as they share a common superclass. For example, imagine you have another subclass called YourString:

```python
class YourString(str):
    pass
```

Now, you can modify the above function to accept arguments of either MyString or YourString:

```python
def modify_string(s: str) -> str:
    # code here
    return result
```

This uses the built-in str class as the superclass, which both MyString and YourString inherit from. This code can accept instances of any subclass that inherits from str, making it more flexible and reusable.

# Conclusion
Subclassing in type hinting lets you create custom data types and use them in a way that makes your code more reliable and reusable. It provides a way to enforce stricter type checking and enables polymorphic behavior. By defining subclasses and using them in type hints, you can create more expressive and powerful code.
