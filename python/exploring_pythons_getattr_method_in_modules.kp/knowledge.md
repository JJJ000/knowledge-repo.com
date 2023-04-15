---
title: Using '__getattr__' in relation to a module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: \_\_getattr\_\_ is used in Python for dynamic attribute access, but it cannot be used directly on modules because modules are already imported and their attributes are pre-defined.
---

**Contents**

[TOC]

Section 1: Introduction to __getattr__ in Python
In Python, the __getattr__ method is a built-in hook method that is called when an attribute lookup on an object fails. It is mainly used to handle dynamic attribute access on an object. When an attribute lookup on an object fails, the interpreter looks for the __getattr__ method in the object's class or subclass, and if found, it is called to handle the failed attribute access.

Section 2: Using __getattr__ on a module in Python
While __getattr__ is commonly used on user-defined classes, it is also possible to use it on modules in Python. When used on a module, __getattr__ is called when an attribute that does not exist in the module is accessed. This can be useful for creating dynamic modules that generate attributes on the fly based on some condition or computation.

Here is an example of using __getattr__ on a module:

```
# mymodule.py

def hello():
    print("Hello, world!")

def __getattr__(name):
    if name == "greet":
        def greet(name):
            print(f"Hello, {name}!")
        return greet
    else:
        raise AttributeError(f"module 'mymodule' has no attribute '{name}'")
```

In the above code, we define a module with a `hello` function and a `__getattr__` hook method. The `__getattr__` method checks if the requested attribute is `greet`, and if so, generates a new function `greet` that takes a name as an argument and prints a personalized greeting. If the requested attribute is not `greet`, an `AttributeError` is raised.

Section 3: Accessing attributes in a module with __getattr__
To access the `hello` function in our `mymodule` example above, we can simply import the module and call the `hello` function as follows:

```
import mymodule

mymodule.hello()
```

This will output the message "Hello, world!" to the console. If we try to access an attribute that does not exist, such as `mymodule.foo`, the `__getattr__` hook in our module will be called, and if the requested attribute is `greet`, a new `greet` function will be generated and returned. We can use this new function like any other function in Python:

```
import mymodule

mymodule.greet("Alice")    # prints "Hello, Alice!"
```

If we try to access an attribute that is not `greet` and is not defined in the module, such as `mymodule.bar`, an `AttributeError` will be raised with a message indicating that the attribute does not exist in the module.

Section 4: Conclusion
Using the `__getattr__` hook method on a module in Python can be a powerful way to create dynamic modules that generate attributes on the fly. By implementing the `__getattr__` method, we can define custom behavior for attribute lookup on our module, which can be useful in many different use cases.
