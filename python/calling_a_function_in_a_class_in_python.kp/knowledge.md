---
title: What is the syntax for calling a function within a class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can call a function within a class in Python by using the class name followed by the function name and any arguments it may take.
---

**Contents**

[TOC]

## Defining the Function

To call a function within a class in Python, first the function must be defined within the class. This is done by using the `def` keyword, followed by the function name, any parameters that should be passed to the function, and then a colon.

```python
class MyClass:
    def my_function(self, param1, param2):
        # Function definition goes here
```

## Calling the Function

Once the function is defined, it can be called within the class. This is done by using the class name, followed by the function name, and any parameters that should be passed to the function.

```python
MyClass.my_function(param1, param2)
```

## Using the `self` Parameter

The `self` parameter is a reference to the class instance itself and is always the first parameter of a function definition in a class. To use the `self` parameter, the function should be called as follows:

```python
my_class_instance = MyClass()
my_class_instance.my_function(param1, param2)
```

## Calling a Function from Another Function

To call a function from another function within a class, the same syntax as above can be used. The only difference is that the `self` parameter should be the first parameter in the function call.

```python
def another_function(self, param1):
    MyClass.my_function(self, param1, param2)
```
