---
title: What is the way to reach the outer class from an inner class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the syntax `OuterClassName.method()` to access the outer class from an inner class in Python.
---

**Contents**

[TOC]

## 1. Overview of Inner Classes in Python

Inner classes are classes declared within the scope of another class in Python. They are useful for grouping related functionality, and can access the attributes and methods of the enclosing class (the "outer class") through an instance of the enclosing class. 

In general, inner classes are used to implement "helper" classes that aren't meant to be used outside of the enclosing class, but still need access to its state.

## 2. Accessing the Outer Class from an Inner Class

There are two ways to access the outer class from an inner class in Python:

### 2.1 Using the `self` Keyword

The `self` keyword in Python refers to the instance of the class that is currently being worked on. In the case of an inner class, `self` refers to the instance of the enclosing class that the inner class is associated with.

To access the outer class from an inner class using `self`, you can simply use `self.<attribute>` or `self.<method>()` to access the attributes or methods of the outer class:

```python
class OuterClass:
    def __init__(self):
        self.outer_attribute = "I am an outer attribute"
        
        class InnerClass:
            def access_outer(self):
                print(self.outer_attribute)
```

In this example, `InnerClass` has access to the `outer_attribute` of its enclosing `OuterClass` instance by using `self.outer_attribute`.

### 2.2 Using a Reference to the Outer Class

Another way to access the outer class from an inner class is to pass a reference to the outer class instance to the inner class as a parameter:

```python
class OuterClass:
    def __init__(self):
        self.outer_attribute = "I am an outer attribute"
        
        class InnerClass:
            def __init__(self, outer):
                self.outer = outer
                
            def access_outer(self):
                print(self.outer.outer_attribute)
                
        self.inner = InnerClass(self)
```

In this example, `InnerClass` takes an instance of `OuterClass` as a parameter and stores it in the `outer` attribute. The `access_outer()` method can then use `self.outer` to access the `outer_attribute` of the enclosing `OuterClass` instance.

## 3. Conclusion

In summary, there are two ways to access the outer class from an inner class in Python: using the `self` keyword, or passing a reference to the outer class instance as a parameter. Both methods provide access to the attributes and methods of the enclosing class, allowing inner classes to be used as "helper" classes that can access the state of their enclosing class.
