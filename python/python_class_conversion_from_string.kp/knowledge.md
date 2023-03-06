---
title: How to transform a string into a Python class object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the built-in `eval()` function to convert a string representation of a class to an actual Python class object.
---

**Contents**

[TOC]

# Introduction

In Python, we can convert a string into a class object using the `eval()` function. The `eval()` function evaluates the string as a Python expression and returns the result.

# Example

Let's say we have a string representation of a class:

```
string_class = '''
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def say_hello(self):
        print("Hello, my name is", self.name)
'''
```

We can convert this string into a class object using `eval()` like this:

```
cls = eval(string_class)
```

Now we can create an instance of the `Person` class and call its methods:

```
p = cls("Alice", 25)
p.say_hello()
```

This will output:

```
Hello, my name is Alice
```

# Explanation

The `eval()` function takes a string and evaluates it as a Python expression. In our case, the string contains the definition of a class, so `eval()` will create a class object based on that definition. We store this class object in the variable `cls`.

We can then use `cls` like any other class object: we can create instances of it (like `p`) and call its methods (like `p.say_hello()`).
