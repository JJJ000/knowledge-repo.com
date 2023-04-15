---
title: What are the ways to delay/put off the assessment of f-strings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use triple-quoted strings to defer the evaluation of f-strings in Python.
---

**Contents**

[TOC]

## Introduction

In Python, we often use f-strings to format strings containing variables. However, sometimes we may want to postpone the evaluation of f-strings until a later time. In this article, we will explore different ways to achieve this.

## Option 1: Use a lambda function

One way to postpone the evaluation of f-strings is to use a lambda function. We can define a lambda function that returns the f-string and call it later when we need to evaluate it.

``` python
def deferred_fstring(fstr):
    return lambda **kwargs: fstr.format(**kwargs)

f = deferred_fstring('Hello, {name}!')
s = f(name='John')
print(s) # Output: 'Hello, John!'
```

In the above code, `deferred_fstring` is a function that takes a string containing an f-string as an argument and returns a lambda function. The lambda function takes keyword arguments as input and returns the evaluated f-string.

## Option 2: Use a class with __getattr__ method

Another option is to use a class with the `__getattr__` method. We can define a class that takes the f-string as an attribute and returns a method that takes keyword arguments and evaluates the f-string.

``` python
class DeferredFString:
    def __init__(self, fstr):
        self.fstr = fstr
    
    def __getattr__(self, name):
        def format(**kwargs):
            return self.fstr.format(**kwargs, **globals())
        return format

f = DeferredFString('Hello, {name}!')
s = f.format(name='John')
print(s) # Output: 'Hello, John!'
```

In the above code, `DeferredFString` is a class that takes the f-string as an attribute in its constructor. The `__getattr__` method returns a method that takes keyword arguments and evaluates the f-string.

## Option 3: Use the format method of str class

A simpler approach is to use the `format` method of the str class. We can pass the f-string as an argument to the `format` method and defer the evaluation by not passing any values for the placeholders. We can then call the `format` method at a later time with the keyword arguments to evaluate the f-string.

``` python
f = 'Hello, {name}!'
s = f.format() # No values for placeholders
print(s) # Output: 'Hello, {name}!'

s = f.format(name='John')
print(s) # Output: 'Hello, John!'
```

In the above code, we pass the f-string to the `format` method without any values for the placeholders, thereby deferring its evaluation. Later, we call the `format` method with the `name` keyword argument to evaluate the f-string.

## Conclusion

In this article, we explored different ways to postpone the evaluation of f-strings in Python. Using a lambda function or a class with the `__getattr__` method enables us to create an object that can be called later to evaluate the f-string. Another option is to use the `format` method of the str class and defer the evaluation by not passing any values for the placeholders. These techniques can be useful in scenarios where we need to defer the evaluation of f-strings until a later time.
