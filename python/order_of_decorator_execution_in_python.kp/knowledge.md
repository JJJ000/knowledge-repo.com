---
title: Order of executing decorators
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Decorators are executed from the innermost to the outermost, following the order in which they are applied to a function or class.
---

**Contents**

[TOC]

# Introduction

Python supports the decorator pattern, which allows you to modify the behavior of an object or method at runtime by dynamically adding new functionality before or after execution. Decorators are functions that take another function as an input and return a new function as an output. When you apply multiple decorators to the same function, you may wonder in which order they will be executed. This article explains the execution order of decorators in Python and provides examples of how to control it.

# Decorating order

The order in which decorators are executed depends on the order in which they appear in the source code. Python applies decorators from the bottom to the top, meaning that the decorator that appears first in the source code will be executed last. For example, consider the following code:

```
@d1
@d2
def foo():
    pass
```

In this case, `foo` is decorated by `d1` and then by `d2`. Therefore, when you call `foo`, Python applies the decorators in the following order: `d2(foo)` -> `d1(d2(foo))`. This is because `d2` is applied first and returns a new function that is then passed to `d1`. Note that if the order of the decorators were reversed, the order of execution would also be reversed.

# Decorator stacking

Decorators can also be stacked on top of each other, meaning that they can be applied to the same function multiple times. When you stack decorators, the order of execution is still determined by the order in which they appear in the source code. For example, consider the following code:

```
@d1
@d1
@d2
def foo():
    pass
```

In this case, `foo` is decorated by `d2` and then by two instances of `d1`. Therefore, when you call `foo`, Python applies the decorators in the following order: `d1(d1(d2(foo)))`. Note that this applies to decorator instances as well, meaning that each instance of `d1` is applied separately.

# Controlling decorator order

If you want to control the order in which decorators are executed, you can do so by defining them as classes instead of functions. When you define a decorator as a class, you have more control over its behavior, including its order of execution. A class-based decorator needs to implement the `__call__` function, which allows it to be used like a regular function. For example, consider the following code:

```
class d1:
    def __init__(self, func):
        self.func = func
    def __call__(self):
        print("d1 before")
        self.func()
        print("d1 after")

class d2:
    def __init__(self, func):
        self.func = func
    def __call__(self):
        print("d2 before")
        self.func()
        print("d2 after")

@d2
@d1
def foo():
    print("foo")

foo()
```

In this case, `d1` and `d2` are defined as classes instead of functions. As a result, they have a more explicit order of execution, which is determined by their definition order in the source code. When you call `foo`, the decorators are applied in the following order: `d1(foo)` -> `d2(d1(foo))`. This is because `d1` is defined first, and then `d2`. Note that by using classes, you have more control over the decorators' behavior, including their order of execution, but you also need to write more code. 

# Conclusion

In summary, the execution order of decorators in Python is determined by the order in which they appear in the source code, from the bottom to the top. If you want to stack decorators, they will be executed in reverse order, and each decorator instance will be applied separately. If you want to control the order of execution, you can define decorators as classes instead of functions and implement the `__call__` function. This allows you to have more control over the decorators' behavior, including their order of execution, but requires more code.
