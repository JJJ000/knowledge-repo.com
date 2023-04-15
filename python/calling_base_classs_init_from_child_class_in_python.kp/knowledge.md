---
title: What is the process to invoke the __init__ method of the parent class from the derived class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To call the Base Class`s \_\_init\_\_ method from the child class in Python, use either super() or ClassName.\_\_init\_\_(self).
---

**Contents**

[TOC]

### 1. Use the super() function to call the parent class's __init__ method 

In Python, the `super()` function can be used to call the parent class's `__init__` method from a child class. This function returns a temporary object of the superclass, which allows us to call its methods.


```python
class Parent:
    def __init__(self, name):
        self.name = name
        
class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age
```

In this example, the `Child` class inherits from the `Parent` class and overrides its `__init__` method. Inside the `Child` class, we use the `super().__init__()` method to call the parent class's `__init__()` method with the same argument `name` that we pass to `Child`'s `__init__()` method. 


### 2. Pass arguments to the super() function

We can also pass additional arguments to the `super().__init__()` method if the parent class's `__init__()` method expects them. 


```python
class Parent:
    def __init__(self, name):
        self.name = name
        
class Child(Parent):
    def __init__(self, name, age, gender):
        super().__init__(name)
        self.age = age
        self.gender = gender
```

In this example, the `Parent` class takes one argument, `name`, in its `__init__()` method, while the `Child` class takes three arguments: `name`, `age`, and `gender`. When we call `super().__init__(name)`, we are passing the `name` argument to the `Parent` class's `__init__()` method. 


### 3. Use the parent class name to call its __init__ method

Alternatively, we can use the parent class name to call its `__init__()` method explicitly, without using the `super()` function:


```python
class Parent:
    def __init__(self, name):
        self.name = name
        
class Child(Parent):
    def __init__(self, name, age, gender):
        Parent.__init__(self, name)
        self.age = age
        self.gender = gender
```

In this example, when we call `Parent.__init__(self, name)`, we are explicitly calling the `__init__()` method of the `Parent` class and passing the `self` and `name` arguments to it.


### 4. Use inheritance to call parent's __init__ method

Finally, if the child class does not define its `__init__()` method, it will automatically inherit the parent class's `__init__()` method:


```python
class Parent:
    def __init__(self, name):
        self.name = name
        
class Child(Parent):
    pass
```

In this case, the `Child` class inherits the `__init__()` method of the `Parent` class, which takes one argument `name`. We do not need to define our `__init__()` method in the `Child` class, as it will inherit the parent's `__init__()` method by default.
