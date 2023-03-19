---
title: What are the ways to prevent circular imports in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Re-organize the code by minimizing dependencies between modules or use dependency injection.
---

**Contents**

[TOC]

## 1. Understanding Circular Imports

Circular imports occur when two or more modules are importing each other, either directly or indirectly. This typically happens in larger Python projects where a module might depend on another module, which in turn depends on the original module.

For instance, consider two modules `module1.py` and `module2.py` where `module1` depends on `module2` and `module2` depends on `module1`. This creates a circular import which can lead to errors such as `NameError`, `AttributeError`, or `ImportError`.

Here's an example of circular import in Python:

```
# module1.py
import module2

# module2.py
import module1
```

## 2. Best Practices to avoid Circular Imports

Circular imports can be tricky to deal with but can be avoided with some careful planning and following best practices. Here are some approaches to avoid circular imports:

### a. Refactor Your Codebase

One of the best solutions to avoid circular imports is to restructure your codebase. This involves breaking up large modules into smaller ones, which can significantly reduce the number of dependencies and make it easier to identify and resolve circular imports.

### b. Use the __name__ Attribute

The `__name__` attribute is a built-in Python attribute that returns the name of the current module. By checking the `__name__` attribute, you can import modules selectively and prevent circular imports.

For example, consider two modules `module1.py` and `module2.py` where `module1.py` depends on `module2.py`. Instead of directly importing `module2` in `module1`, you can use the `__name__` attribute to check whether the module is being imported directly or indirectly.

```
# module1.py
if __name__ == '__main__':
    import module2

# module2.py
import module1
```

### c. Move Imports Inside Functions

One way to avoid circular imports is to move imports inside functions instead of at the module level. This ensures that the circular dependency only occurs when the function is called and not during module imports.

For example:

```
# module1.py
def some_function():
    from module2 import some_value

# module2.py
def some_other_function():
    from module1 import some_other_value
```

### d. Use Absolute Imports

Using absolute imports instead of relative imports is another way to avoid circular imports. Absolute imports specify the full path to the module, rather than relying on relative module paths that can lead to circular imports.

For example:

```
# module1.py
from package.module2 import some_value

# module2.py
from package.module1 import some_other_value
```

## 3. Conclusion

Circular imports in Python can cause issues and make your code harder to maintain. By restructuring your codebase, using the `__name__` attribute, or moving imports inside functions, you can avoid circular dependencies and write more maintainable and scalable code.
