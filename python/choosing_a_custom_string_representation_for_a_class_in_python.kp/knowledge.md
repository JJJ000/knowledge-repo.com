---
title: What approach should I take to select a personalized string representation for the class itself rather than for its instances?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Define the `\_\_repr\_\_` method on the class object.
---

**Contents**

[TOC]

## The `__str__` method

To define a custom string representation for instances of a class, we use the `__str__` method. This method is called when we try to convert an instance of the class to a string using the `str()` function or string formatting methods.

```python
class MyClass:
    def __init__(self):
        self.foo = 42

    def __str__(self):
        return f"MyClass(foo={self.foo})"
```

In this example, we define a class `MyClass` with an attribute `foo` set to 42. The `__str__` method returns a string representation of the instance with the format `MyClass(foo=<value of foo>)`.

However, this only applies to instances of the class, not the class itself. To define a custom string representation for the class itself, we need to define a `__str__` method for the class.


## Defining a `__str__` method for the class

To define a custom string representation for the class itself, we need to define a `__str__` method for the class. This method is similar to the `__str__` method for instances, but it takes the class as an argument instead of an instance.

```python
class MyClass:
    def __init__(self):
        self.foo = 42

    def __str__(self):
        return f"MyClass(foo={self.foo})"

    @classmethod
    def __str__(cls):
        return "MyClass"
```

In this example, we define a `__str__` method for the class `MyClass` using the `@classmethod` decorator. This method simply returns the string `"MyClass"`. 

Note that this method overrides the `__str__` method for instances of the class. To avoid this, we should define a different method name for the class string representation.


## Defining a custom method for the class string representation

To avoid overriding the `__str__` method for instances of the class, we can define a custom method for the class string representation.

```python
class MyClass:
    def __init__(self):
        self.foo = 42

    def __str__(self):
        return f"MyClass(foo={self.foo})"

    @classmethod
    def class_name(cls):
        return "MyClass"
```

In this example, we define a method `class_name` for the class `MyClass`. This method simply returns the string `"MyClass"`. We can use this method to get the string representation of the class.

```python
>>> MyClass.class_name()
"MyClass"
```

Note that this method does not override the `__str__` method for instances of the class, so we can still use it to get the string representation of instances.

```python
>>> obj = MyClass()
>>> str(obj)
"MyClass(foo=42)"
```


## Conclusion

To define a custom string representation for a class itself, we can define a `__str__` method or a custom method for the class string representation. The `__str__` method for the class overrides the `__str__` method for instances, so we should define a different method name to avoid conflicts.
