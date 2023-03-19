---
title: Is it possible to call a staticmethod within the body of a class in Python version less than or equal to 3.9?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Yes, it is possible to call a class static method within the class body in Python version <= 3.9.
---

**Contents**

[TOC]

Introduction:

In Python programming language, we can define a static method within a class. In general, static methods are not associated with an instance of the class rather they can be accessed through the class itself. However, in Python versions <= 3.9, calling a class static method within the class body could raise an error. Let's discuss this phenomenon in detail.

Problem Description:

In Python versions <= 3.9, calling a class static method within the class body is not allowed as it would raise a NameError. Here is an example code snippet that will clarify the issue.

```
class MyClass:
    @staticmethod
    def my_staticmethod():
        return "Hello from static method"
        
    my_static_ref = my_staticmethod()
```

In the above code snippet, we are trying to call a static method "my_staticmethod" of "MyClass" while defining a class attribute "my_static_ref". This will result in a NameError as the static method is not yet defined at this point.

Solution:

1. Use a Metaclass:

One way to avoid the NameError is by using a metaclass to define the class. Here is an example that demonstrates how to use a metaclass to define a class with a static method and a class attribute.

```
class MyMeta(type):
    def __new__(cls, name, bases, dct):
        dct['my_static_ref'] = cls.my_staticmethod()
        return super().__new__(cls, name, bases, dct)

class MyClass(metaclass=MyMeta):
    @staticmethod
    def my_staticmethod():
        return "Hello from static method"
```

In the above code, we defined a metaclass "MyMeta" that adds a class attribute "my_static_ref" to the "MyClass" class. The metaclass uses the static method "my_staticmethod" to define the value of the class attribute. This ensures that the static method is already defined when the class attribute is initialized.

2. Move the call to the static method:

Another way to avoid the NameError is to move the call to the static method outside the class body. Here is an example that demonstrates this approach.

```
class MyClass:
    @staticmethod
    def my_staticmethod():
        return "Hello from static method"

MyClass.my_static_ref = MyClass.my_staticmethod()
```

In the above code, we defined the "my_static_ref" class attribute outside the class body, after the static method "my_staticmethod" has already been defined. This ensures that the static method is available when the class attribute is initialized.

Conclusion:

In Python versions <= 3.9, calling a class static method within the class body is not allowed as it would raise a NameError. We can use a metaclass or move the call to the static method outside the class body to avoid this issue.
