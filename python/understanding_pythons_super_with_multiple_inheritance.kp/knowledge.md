---
title: What is the role of super() in Python when dealing with multiple inheritance?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Python`s super() allows for the parent classes of a child class to be called in a specific order when multiple inheritance is used.
---

**Contents**

[TOC]

# Overview

Python's `super()` function is a useful tool for working with multiple inheritance. It allows a class to access methods from its parent classes without explicitly specifying them. It is especially useful when dealing with multiple inheritance, as it can help to avoid name conflicts and other issues.

# Usage

When using `super()`, the first argument should always be the current class. The second argument should be the parent class from which the method is being called. The third argument is optional, and is used to specify the name of the method being called.

For example, if a class `Child` inherits from two parent classes `Parent1` and `Parent2`, the following code would call the `foo()` method from `Parent1`:

```
super(Child, Parent1).foo()
```

# Benefits

The main benefit of using `super()` is that it allows for a more concise and readable code. It also helps to avoid name conflicts and other issues that can arise from multiple inheritance.

Furthermore, since `super()` allows for dynamic method resolution, it can be used to support cooperative multiple inheritance. This means that the order in which the parent classes are specified does not matter, as the method resolution will always be done in the correct order.
