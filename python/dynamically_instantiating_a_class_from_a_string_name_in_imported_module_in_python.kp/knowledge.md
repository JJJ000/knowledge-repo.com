---
title: Can a dynamically imported module create an instance of a class using a string representing the class name?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `getattr()` function to get a reference to the class from the module and then instantiate the class using the regular syntax.
---

**Contents**

[TOC]

1. Introduction

Dynamic instantiation of a class refers to creating an instance of a class at runtime, without knowing the name of the class at compile-time. In Python, this can be done using the built-in `type()` function. The `type()` function takes three arguments: the name of the class, a tuple of its base classes, and a dictionary containing its attributes and methods. However, if the class is defined in a dynamically imported module, we need to first import the module before we can create an instance of the class.

2. Importing a dynamically imported module

To import a dynamically imported module in Python, we can use the built-in `importlib` module. We can use the `import_module()` function to import a module by its name, which is a string. For example, to import a module called `example_module`, we can use the following code:

```python
import importlib

module_name = 'example_module'
module = importlib.import_module(module_name)
```

This will import the `example_module` module and assign it to the `module` variable.

3. Dynamically instantiating a class in a dynamically imported module

Once we have imported the module, we can dynamically instantiate a class from it using the `getattr()` function. The `getattr()` function takes two arguments: the object (in this case, the module object) and the name of the attribute we want to get (in this case, the name of the class). For example, if we have a module called `example_module` that contains a class called `ExampleClass`, we can dynamically instantiate that class using the following code:

```python
import importlib

module_name = 'example_module'
class_name = 'ExampleClass'

module = importlib.import_module(module_name)
class_obj = getattr(module, class_name)
instance = class_obj()
```

This will import the `example_module` module, get a reference to the `ExampleClass` class object, and create a new instance of it.

4. Conclusion

Dynamic instantiation of a class from a dynamically imported module in Python can be done using the `importlib` module to import the module by name, and the `getattr()` function to get a reference to the class object by name. Once we have the class object, we can use the `type()` function to create new instances of the class.
