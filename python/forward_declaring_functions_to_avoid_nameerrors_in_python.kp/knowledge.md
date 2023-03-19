---
title: What is the method for forward-declaring a function to prevent "nameerror"s for functions that are defined afterwards?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `pass` keyword to create an empty function with the same name and signature as the function you wish to define later.
---

**Contents**

[TOC]

# Introduction
Python executes code from top to bottom, which means that if you try to call a function before it has been defined, you will receive a `NameError`. In this guide, we will discuss how to use forward-declarations to avoid `NameError`s for functions defined later in Python.

# What is a Forward-Declaration?
A forward-declaration is a reference to a function that has not been defined yet. It allows you to use the function without having to define it beforehand. This is useful when you have functions that call each other, or when you want to define functions that use other functions defined later in the code.

# How to Forward-Declare a Function
To forward-declare a function, you can simply use the `pass` keyword to define an empty function with the same name as the function you want to call later. Here is an example:

```python
def function1():
    function2()
    
def function2():
    pass
    
function1()  # This will work fine
```

In this example, we forward-declared `function2` by defining an empty function with the same name.

# When to Use Forward-Declarations
Forward-declarations can be useful in a variety of scenarios, including when you have a large codebase with many interdependent functions, or when you have functions that call each other recursively. However, it is important to note that overuse of forward-declarations can make your code difficult to read and maintain, so it is important to use them judiciously.

# Conclusion
Forward-declarations are a useful tool for avoiding `NameError`s in Python. By using forward-declarations, you can define functions that call each other or use other functions defined later in the code without running into `NameError`s. However, it is important to use forward-declarations judiciously to avoid making your code difficult to read and maintain.
