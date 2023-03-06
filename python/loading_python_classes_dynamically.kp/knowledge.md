---
title: What is the procedure for loading a Python class dynamically?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the built-in `importlib` module to import the module containing the class, and then use the `getattr()` function to retrieve the class object by name.
---

**Contents**

[TOC]

# Introduction

In Python, you can dynamically load a class at runtime without importing it at the beginning of your script. This can be useful when you need to load classes based on user input or when you want to improve the startup time of your application by only importing the necessary classes.

# Using the `importlib` module

Python's built-in `importlib` module provides a way to dynamically load modules and classes. Here's an example of how you can use it to load a class:

```python
import importlib

class_name = "MyClass"
module_name = "my_module"

module = importlib.import_module(module_name)
my_class = getattr(module, class_name)
```

In this example, we first import the `importlib` module. We then specify the name of the class we want to load (`MyClass`) and the name of the module it is defined in (`my_module`). We use the `import_module` function to load the module, and then use `getattr` to get the class by name.

# Using `type` to create a class

Another way to dynamically load a class is to use the `type` function to create the class at runtime. Here's an example:

```python
class_dict = {
    'attr1': 42,
    'attr2': 'hello',
}

MyClass = type('MyClass', (object,), class_dict)
```

In this example, we define a dictionary that contains the attributes we want our class to have. We then use the `type` function to create the class, passing in the name of the class (`MyClass`), a tuple of base classes (in this case just `object`), and the dictionary of class attributes.

# Conclusion

Dynamically loading classes can be a powerful tool in your Python toolbox. Whether you choose to use the `importlib` module or the `type` function, you can load classes at runtime based on user input or other factors, without having to import everything at the beginning of your script.
