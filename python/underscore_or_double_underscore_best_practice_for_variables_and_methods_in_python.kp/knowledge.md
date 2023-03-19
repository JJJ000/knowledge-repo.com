---
title: Differences between variables and methods with single underscore and double underscore
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: A single underscore before a variable or method name signifies it as `weakly private` while a double underscore signifies it as `strongly private` in Python.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, underscores are used in variable and method names as a way to convey meaning to other programmers. In particular, underscores can be used for naming conventions, to indicate that a variable or method is private or special, or to separate words in a name.

There are two main types of underscores used in Python: single underscores and double underscores. In this article, we will focus on the differences between these two types and explore when to use each one.

Section 2: Single Underscore (_)

The single underscore is generally used as a naming convention for variables or methods that are not meant to be accessed outside of a certain scope. For example, if you have a function that returns an internal value that is not part of the public interface, you might name the variable that holds this value with a single underscore:

```python
def calculate_something(x, y):
    _internal_value = x + y
    return _internal_value * 2
```

This tells other programmers that they should not rely on this variable being available, but it also allows you to access it within the same module or class.

In addition to naming conventions, single underscores can also be used to separate words in variable or method names. This is especially useful for long names:

```python
my_long_variable = 42
```

Section 3: Double Underscore (__)

Double underscores are used for special methods or attributes in Python. These methods have reserved names and are called by the Python interpreter in specific situations. For example, if you define a class with a method called `__len__`, that method will be called when you use the built-in `len` function on an instance of that class:

```python
class MyClass:
    def __len__(self):
        return 42

my_instance = MyClass()
print(len(my_instance))  # prints 42
```

In addition to special methods, double underscores can also be used to create name mangling. This is a way of making attributes or methods private to a class by prefixing them with double underscores. When this is done, the name of the attribute or method is "mangled" with the name of the class:

```python
class A:
    def __init__(self):
        self.__private_variable = 42
    
class B(A):
    def print_private_variable(self):
        print(self.__private_variable)

b = B()
b.print_private_variable()  # raises an AttributeError
```

In this example, we create a class `A` with a private variable that is prefixed with double underscores. When we define a subclass of `A` called `B`, we try to access this variable in a method. However, because the variable is name-mangled with the name of the class, we get an `AttributeError` when we try to access it.

Section 4: Conclusion

In conclusion, underscores are an important part of Python's naming conventions and can be used to convey meaning to other programmers. Single underscores are used for naming conventions and word separation, while double underscores are used for special methods and attributes, as well as name mangling.

When using underscores, it is important to be consistent with your naming conventions and to follow common practices in the Python community. This will make your code more readable and easier to maintain in the long run.
