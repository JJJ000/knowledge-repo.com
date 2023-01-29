---
title: What are static methods in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Static methods in Python are methods that do not require an instance of the class to be used.
---

**Contents**

[TOC]

#### What are static methods?
Static methods are methods that are bound to a class rather than its object. It doesn't require a reference to the class instance object (self) to be passed as the first argument.

#### How to define a static method
Static methods are defined using the @staticmethod decorator.

```python
class MyClass:
    @staticmethod
    def my_static_method():
        # code here
```

#### Advantages of static methods
- Static methods are more organized and easier to read than regular methods, since they are separated from the class's other methods.
- They are also more efficient, since they do not require an instance of the class to be created before they can be called.

#### Disadvantages of static methods
- Static methods are less flexible than regular methods, since they cannot access the instance variables of the class.
- They can also be difficult to test, since they cannot be mocked or stubbed.
