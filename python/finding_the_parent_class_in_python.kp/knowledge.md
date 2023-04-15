---
title: What is the method to retrieve the parents of a Python class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: One way to get the parents of a Python class is to access the class`s \_\_bases\_\_ attribute, which returns a tuple of the class`s parent classes.
---

**Contents**

[TOC]

### Section 1: Understanding parent classes in Python

In Python, classes can inherit attributes and methods from existing classes. The existing class is called the parent class, while the new class that inherits from it is called the child class. 

When a child class inherits from a parent class, it can access all the attributes and methods of the parent class. This is useful for creating new classes that have some of the functionality of existing classes, but with additional features or modifications.

### Section 2: Using the built-in __bases__ attribute

In Python, you can access the parent classes of a given class using the built-in `__bases__` attribute. This attribute returns a tuple of the parent classes, in order from the most immediate parent to the most distant ancestor.

Here's an example of how to use the `__bases__` attribute to get the parent classes of a class named `MyClass`:

```python
class ParentClass:
    pass

class MyClass(ParentClass):
    pass

print(MyClass.__bases__)
```

This will output:

```
(<class '__main__.ParentClass'>,)
```

In this example, `MyClass` inherits from `ParentClass`, so its `__bases__` attribute returns a tuple containing only `ParentClass`.

### Section 3: Using the inspect module

Another way to get the parent classes of a class in Python is to use the `inspect` module. This is a more general-purpose approach that can be used to inspect any object in Python, not just classes.

Here's an example of how to use the `inspect` module to get the parent classes of a class named `MyClass`:

```python
import inspect

class ParentClass:
    pass

class MyClass(ParentClass):
    pass

print(inspect.getmro(MyClass))
```

This will output:

```
(<class '__main__.MyClass'>, <class '__main__.ParentClass'>, <class 'object'>)
```

In this example, we use the `inspect.getmro()` function to get the method resolution order of `MyClass`. The method resolution order is a list of classes that Python searches when looking up an attribute or method. It starts with the class itself (`MyClass`), followed by its parent classes (in this case, `ParentClass`), and finally the `object` class that all classes inherit from.

### Section 4: Conclusion

In conclusion, there are two main ways to get the parent classes of a Python class:

- Using the built-in `__bases__` attribute
- Using the `inspect` module

Both methods will give you a tuple or list of the parent classes of a given class. Depending on your use case, one method may be more appropriate than the other.
