---
title: What is the process of invoking a method from another method in the context of static methods?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To call a static method from another method in Python, use the class name followed by the static method name, separated by a dot.
---

**Contents**

[TOC]

# Introduction
Static methods are methods that are bound to the class and not the instance of the class. These methods do not require an instance of the class to be called. In this article, we will discuss how to call a method from another method in Python.

# Defining Static Methods
To define a static method in Python, we use the @staticmethod decorator. This decorator must be placed above the method definition to indicate that the method is a static method. Static methods take no special arguments and cannot access instance attributes or methods.

```python
class MyClass:
    @staticmethod
    def my_static_method():
        print("This is a static method")
```

# Calling Static Methods
Since static methods are bound to the class and not the instance of the class, they are called directly on the class itself. To call a static method, we simply use the class name followed by the method name.

```python
MyClass.my_static_method()
```

# Calling a Method from Another Method
To call a method from another method in Python, we simply call the method as we would normally. If the method is a static method, we call it using the class name.

```python
class MyClass:
    @staticmethod
    def my_static_method():
        print("This is a static method")

    @staticmethod
    def another_static_method():
        MyClass.my_static_method()
```

In this example, we have defined two static methods. The second method, another_static_method, calls the first method, my_static_method, by calling it using the class name MyClass. 

# Conclusion
In this article, we discussed how to call a method from another method in Python when dealing with static methods. We looked at how to define static methods, how to call static methods, and how to call a method from another method when dealing with static methods.
