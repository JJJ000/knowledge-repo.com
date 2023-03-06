---
title: What is the way to implement method overloading in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Python doesn`t support method overloading, so we can`t use it directly, but we can use default argument values to achieve similar functionality.
---

**Contents**

[TOC]

## Introduction to Method Overloading in Python

Method overloading is a feature that allows multiple methods with the same name to be defined in a class. The method to be called is determined by the number, types, and order of the arguments passed to it. Python doesn't natively support method overloading, but there are several ways to achieve it.


## Using Default Argument

The simplest way to achieve method overloading in Python is by using default arguments. We can define a method with default arguments and then call the method with specific arguments. If the specific argument is not provided, the method will use the default argument.

```python
class MyClass:
    def mymethod(self, arg1, arg2=None):
        if arg2:
            print(arg1, arg2)
        else:
            print(arg1)
```

In the above example, we have defined a method `mymethod` with two arguments where `arg2` is set as `None` by default. If `arg2` is provided, the method will execute the first block of code, otherwise, the second block of code will execute.

## Using Variable Arguments

Another way to achieve method overloading is by using variable arguments. Python allows us to define methods with `*args` and `**kwargs` parameters, which can accept any number of arguments.

```python
class MyClass:
    def mymethod(self, *args):
        if len(args) == 1:
            print(args[0])
        elif len(args) == 2:
            print(args[0], args[1])
        else:
            print("Invalid number of arguments")

obj = MyClass()
obj.mymethod(1)
obj.mymethod(1, 2)
```

In the above example, we have defined a method `mymethod` with `*args` parameter, which means it can accept any number of arguments. We have used an `if-elif` condition to check the number of arguments passed to the method and print them accordingly.

## Using Multiple Dispatch Decorator

We can also achieve method overloading in Python using the `multipledispatch` library, which provides a `@dispatch` decorator that allows us to define multiple functions with the same name but with different signatures.

```python
from multipledispatch import dispatch

class MyClass:
    @dispatch(int)
    def mymethod(self, arg1):
        print(arg1)

    @dispatch(int, int)
    def mymethod(self, arg1, arg2):
        print(arg1, arg2)

obj = MyClass()
obj.mymethod(1)
obj.mymethod(1, 2)
```

In the above example, we have used the `@dispatch` decorator to define multiple functions with the same name `mymethod` but with different signatures. The decorator determines which method to call based on the types of the arguments passed to it.


## Conclusion

Method overloading is not a native feature of Python but can be achieved using default arguments, variable arguments, or multiple dispatch decorators. It allows us to define multiple methods with the same name but with different signatures, making our code more readable and maintainable.
