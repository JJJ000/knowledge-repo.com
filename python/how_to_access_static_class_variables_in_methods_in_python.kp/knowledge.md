---
title: What is the method to access class variables that are "static" from within methods?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can access the static class variables using the class name followed by a dot and the variable name within the method.
---

**Contents**

[TOC]

#### Defining a "static" class variable in Python

In Python, there is no such thing as a "static" class variable like in some other programming languages. However, you can create class-level attributes that are shared among instances of the class. You can define them by putting them directly inside the class definition block, but outside of any method or initialization function. Here is an example:

```python
class MyClass:
    my_variable = 42
```

This creates a class `MyClass` with a class-level attribute `my_variable` initialized to 42. Every instance of this class will have access to this attribute.

#### Accessing "static" class variables from within methods

To access a class-level attribute from within a method of the same class, you can use either the class name or the `self` reference. Here are two equivalent ways of accessing the `my_variable` attribute in the `my_method` of `MyClass`:

```python
class MyClass:
    my_variable = 42

    def my_method(self):
        print(self.my_variable)     # using self reference
        print(MyClass.my_variable)  # using class name
```

Both `self.my_variable` and `MyClass.my_variable` will access the same attribute, but the `self` reference is more flexible because it allows subclasses to override `my_variable` with their own value.

#### Modifying "static" class variables from within methods

To modify a class-level attribute from within a method of the same class, you can use the same two approaches as above. However, if you want the change to apply to all instances of the class (not just the current instance), you should use the class name. Here is an example:

```python
class MyClass:
    my_variable = 42

    def my_method(self):
        MyClass.my_variable = 10

print(MyClass.my_variable)  # prints 42
obj = MyClass()
obj.my_method()
print(MyClass.my_variable)  # prints 10
```

This modifies the `my_variable` attribute of the `MyClass` class and not just the instance attribute of `obj`.

#### Avoiding naming clashes with "static" class variables

Since class-level attributes are shared among instances, you need to be careful not to accidentally overwrite them with instance attributes of the same name. One way to avoid this is to use a naming convention for class-level attributes, such as prefixing them with `_`. Here is an example:

```python
class MyClass:
    _my_variable = 42

    def my_method(self):
        print(self._my_variable)

    def set_my_variable(self, value):
        self._my_variable = value

obj = MyClass()
obj.my_method()           # prints 42
obj.set_my_variable(10)
obj.my_method()           # prints 10
print(MyClass._my_variable)  # prints 42
```

Using `_my_variable` as the class-level attribute name signals to other programmers that it should not be modified by instances of the class.
