---
title: Can you explain the mechanics of lexical closures?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Lexical closures in Python allow inner functions to access variables from outer functions, even after the outer function has returned.
---

**Contents**

[TOC]

# Overview

A closure is a technique that allows a function to access and manipulate variables from its enclosing scope, even after that scope has been destroyed. In Python, closures are implemented using nested function definitions.

# Creating a Closure

To create a closure in Python, we define a function inside another function, and then return the inner function. The inner function can reference and modify variables from the outer function's local scope, even after the outer function has finished executing. 

Here's an example:

```python
def outer(a):
    def inner(b):
        return a + b
    return inner

closure = outer(5)
result = closure(3)
print(result)  # Output: 8
```

In this example, the `outer` function takes an argument `a` and returns an inner function `inner`, which takes an argument `b` and adds it to `a`. We then call `outer` with an argument of 5, which returns the `inner` function. Finally, we call `closure(3)` to add 3 to `a` (which is 5) and get a result of 8.

# Modifying Variables in a Closure

A closure can also modify variables from the enclosing scope. Here's an example:

```python
def counter():
    count = 0
    
    def inner():
        nonlocal count
        count += 1
        return count
        
    return inner

c = counter()
print(c())  # Output: 1
print(c())  # Output: 2
print(c())  # Output: 3
```

In this example, the `counter` function returns an inner function `inner`, which increments a local variable `count` each time it is called. Notice that we use the `nonlocal` keyword inside `inner` to tell Python that we want to modify the `count` variable from the outer function's scope, rather than creating a new local variable.

# Benefits and Limitations of Closures

Closures allow us to create functions that have persistent state across multiple function calls, without polluting the global namespace with variables. They also allow us to parameterize functions with extra data that is not available when the function is first defined.

However, closures can also lead to subtle bugs and performance issues if not used carefully. For example, if a closure modifies a variable that is shared across multiple threads, it can lead to race conditions and other synchronization problems.

Overall, closures are a powerful feature of Python that can be used to create complex and customizable functions. However, they should be used judiciously and with care to avoid potential pitfalls.
