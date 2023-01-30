---
title: What is the syntax for annotating a method with the type of the class it is contained in?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can type hint a method with the type of the enclosing class in Python by using the syntax `self` or `cls` for the type.
---

**Contents**

[TOC]

## Using Type Hints
Type hints can be used to specify the type of a method's parameters and return value. In the case of a method belonging to a class, the type of the enclosing class can be specified as the type for the method.

## Syntax
The syntax for type hinting a method with the type of the enclosing class is as follows:

```
def method_name(self) -> ClassName:
    # Method body
```

Where `method_name` is the name of the method, `ClassName` is the name of the enclosing class, and `# Method body` is the body of the method.

## Example
For example, consider a class `Foo` with a method `bar`:

```
class Foo:
    def bar(self) -> Foo:
        # Method body
```

Here, the type hint for the `bar` method is `Foo`, indicating that the method belongs to the `Foo` class.
