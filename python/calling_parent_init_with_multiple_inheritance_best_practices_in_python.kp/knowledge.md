---
title: What is the correct method for invoking the __init__ of a parent class when using multiple inheritance?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The correct way to call the parent class \_\_init\_\_ with multiple inheritance in Python is to explicitly call the parent class \_\_init\_\_ in the child class \_\_init\_\_.
---

**Contents**

[TOC]

### Section 1: Overview
When a class inherits from multiple parent classes, the __init__ method of the child class must call the __init__ method of each parent class. This is done to ensure that all of the attributes of the parent classes are initialized properly.

### Section 2: Syntax
The syntax for calling the __init__ method of the parent classes is as follows:

```python
class ChildClass(ParentClass1, ParentClass2):
    def __init__(self, *args, **kwargs):
        ParentClass1.__init__(self, *args, **kwargs)
        ParentClass2.__init__(self, *args, **kwargs)
        # Any other initialization code
```

### Section 3: Example
For example, if we have two parent classes, ParentClass1 and ParentClass2, and a child class, ChildClass, that inherits from both of them, the code might look like this:

```python
class ParentClass1:
    def __init__(self, value1):
        self.value1 = value1

class ParentClass2:
    def __init__(self, value2):
        self.value2 = value2

class ChildClass(ParentClass1, ParentClass2):
    def __init__(self, value1, value2, value3):
        ParentClass1.__init__(self, value1)
        ParentClass2.__init__(self, value2)
        self.value3 = value3
```

### Section 4: Conclusion
In conclusion, when using multiple inheritance, the __init__ method of the child class must call the __init__ methods of each parent class in order to ensure that all of the attributes of the parent classes are initialized properly. The syntax for doing this is as shown above.
