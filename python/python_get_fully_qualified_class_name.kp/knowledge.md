---
title: Find the complete name of the class to which an object belongs in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To get fully qualified class name of an object in Python, we can use the \_\_class\_\_.\_\_name\_\_ attribute.
---

**Contents**

[TOC]

## Using the __class__ attribute

The most straightforward way of obtaining the fully qualified class name of an object in Python is by accessing the `__class__` attribute of the object and getting its `__name__` property, which gives the class name without modules. To get the fully qualified name, you can access the `__module__` attribute of the class, which gives the name of the module where the class is defined, and concatenate it with the class name.


```python
class MyClass:
    pass

my_object = MyClass()

class_name = my_object.__class__.__name__
module_name = my_object.__class__.__module__
fully_qualified_class_name = f"{module_name}.{class_name}"

print(fully_qualified_class_name) # prints "__main__.MyClass"
```


## Using the type() function

Another way of obtaining the fully qualified class name of an object is by using the `type()` function on the object and getting its `__name__` and `__module__` attributes, as shown in the previous example. This method allows you to get the class name and module name of an object dynamically, without explicitly accessing its `__class__` attribute. 


```python
class MyClass:
    pass

my_object = MyClass()

class_name = type(my_object).__name__
module_name = type(my_object).__module__

fully_qualified_class_name = f"{module_name}.{class_name}"

print(fully_qualified_class_name) # prints "__main__.MyClass"
```


## Using importlib

If you only have the class name as a string and want to obtain its fully qualified name dynamically, you can use the `importlib` library to load the module where the class is defined and get its fully qualified name.


```python
import importlib

class_name = "MyClass"

module = importlib.import_module("__main__")
class_ = getattr(module, class_name)

class_name = class_.__name__
module_name = class_.__module__

fully_qualified_class_name = f"{module_name}.{class_name}"

print(fully_qualified_class_name) # prints "__main__.MyClass"
```

## Using __qualname__

In Python3, you can also use the `__qualname__` attribute of a class to access the qualified name of a class like this:

```python
class MyClass:
    class NestedClass:
        pass

fully_qualified_class_name = MyClass.NestedClass.__qualname__

print(fully_qualified_class_name) # prints "MyClass.NestedClass"
```

This allows to get the entire namespace of class including any outer classes.
