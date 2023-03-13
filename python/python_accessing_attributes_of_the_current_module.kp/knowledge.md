---
title: What is the method for acquiring the attributes of the current module in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `globals()` function to get a reference to the current module`s attributes.
---

**Contents**

[TOC]

## Introduction

In Python, a module is a file that contains Python definitions and statements. A module can define functions, classes and variables, and can also include runnable code. When a module is imported, its contents become available as attributes of the imported module object. In some cases, it may be necessary to access the attributes of the current module from within the module's code. This can be accomplished using a variety of techniques, which will be discussed in this article.

## Using the __dict__ attribute

One way to access the attributes of the current module is to use the __dict__ attribute of the module object. This attribute is a dictionary that maps the names of the module's attributes to their values. To access an attribute, simply use its name as a key in the dictionary.

```python
import sys

module_dict = sys.modules[__name__].__dict__
print(module_dict['x']) # prints the value of the 'x' variable
```

In this example, the __name__ attribute of the current module is used to get a reference to the module object, which is then used to access the __dict__ attribute. The value of the 'x' variable is then obtained by indexing the dictionary using the string 'x' as a key.

## Using globals()

Another way to access the attributes of the current module is to use the built-in globals() function. This function returns a dictionary that contains the current global namespace, which includes all the module's attributes.

```python
x = 1
globals_dict = globals()
print(globals_dict['x']) # prints the value of the 'x' variable
```

In this example, the globals() function is used to obtain a reference to the global namespace, which is then used to access the 'x' variable.

## Using the inspect module

The inspect module provides a variety of functions for inspecting and analyzing Python code. One of these functions, called getmembers(), can be used to obtain a list of (name, value) pairs for all the attributes of an object.

```python
import inspect

module_members = inspect.getmembers(sys.modules[__name__])
for member in module_members:
    print(member) # prints the name and value of each module attribute
```

In this example, the getmembers() function is used to obtain a list of all the (name, value) pairs for the current module. The resulting list is then printed to the console.

## Conclusion

In this article, we have discussed three techniques for accessing the attributes of the current module in Python. These include using the __dict__ attribute of the module object, using the globals() function, and using the getmembers() function from the inspect module. Depending on the specific use case, one of these techniques may be more appropriate than the others.
