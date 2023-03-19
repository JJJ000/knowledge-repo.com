---
title: Retrieve the memory address of a Python variable
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To print the memory address of a Python variable, you can use the id() function.
---

**Contents**

[TOC]

## Introduction

In Python, it is possible to obtain the memory address of a variable using a built-in function called `id()`. This function returns an integer that represents the memory address of the given variable. In this article, we will cover how to print the memory address of a Python variable in detail.


## Printing the Memory Address of a Python Variable

To print the memory address of a Python variable, you can use the `id()` function. Here is an example:

```python
x = 5
print(id(x))
```

This will output something like:

```
4547562904
```

The integer returned by `id(x)` is the memory address of the integer object `5` in memory. This number may differ each time you run the program, as the memory manager may allocate memory at different locations each time.

It is important to note that `id()` returns a memory address in hexadecimal format, which is commonly denoted by a prefix of `0x`. If you want to print the memory address in decimal format, you can use the `hex()` built-in function:

```python
x = 5
print(int(hex(id(x)), 16))
```

This will output `4547562904` as an integer.

## Printing the Memory Address of a Specific Object Instance

If you want to print the memory address of a specific instance of an object, you can use the `id()` function on that instance. For example, let's say you have an instance of a `Person` class:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 30)
```

To print the memory address of `person1`, you can simply call `id(person1)`:

```python
print(id(person1))
```

This will output something like:

```
4547563552
```

## Conclusion

Printing the memory address of a Python variable is a useful debugging technique when you want to know the exact location of a variable in memory. The `id()` function makes this task easy and straightforward. By using this function, you can obtain the memory address of any Python object and use it to analyze its behavior in memory.
