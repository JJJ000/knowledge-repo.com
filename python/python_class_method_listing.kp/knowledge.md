---
title: What are the methods available in a Python class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the dir() function to get a list of methods in a Python class.
---

**Contents**

[TOC]

### Using dir()

The `dir()` built-in function can be used to get a list of all methods in a Python class.

```python
class MyClass:
    def method1(self):
        pass
    def method2(self):
        pass

methods = dir(MyClass)
print(methods)
# Output: ['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'method1', 'method2']
```

### Using inspect

The `inspect` module can be used to get a list of all methods in a Python class.

```python
import inspect

class MyClass:
    def method1(self):
        pass
    def method2(self):
        pass

methods = [func for func in inspect.getmembers(MyClass, predicate=inspect.isfunction) if not func[0].startswith('_')]
print(methods)
# Output: [('method1', <function MyClass.method1 at 0x000001A7B2C2F620>), ('method2', <function MyClass.method2 at 0x000001A7B2C2F6A8>)]
```

### Using class.__dict__

The `class.__dict__` attribute can be used to get a list of all methods in a Python class.

```python
class MyClass:
    def method1(self):
        pass
    def method2(self):
        pass

methods = [func for func in MyClass.__dict__.keys() if not func.startswith('_')]
print(methods)
# Output: ['method1', 'method2']
```

### Using class.__dict__.items()

The `class.__dict__.items()` attribute can be used to get a list of all methods in a Python class.

```python
class MyClass:
    def method1(self):
        pass
    def method2(self):
        pass

methods = [func for func, obj in MyClass.__dict__.items() if inspect.isfunction(obj)]
print(methods)
# Output: ['method1', 'method2']
```
