---
title: What is the difference between 'import module' and 'from module import'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: It depends on the desired functionality; use `import module` to import the module as a whole, or use `from module import` to import specific functions, classes, or variables from the module.
---

**Contents**

[TOC]

# import module

The `import module` statement is used to import a single module. This statement will make the module available to the current namespace, allowing you to access the module’s contents using dot notation.

For example, if you want to import a module named `math`, you can use the following statement:

```python
import math
```

# from module import

The `from module import` statement is used to import specific attributes or functions from a module. This statement allows you to access the module’s contents without having to use dot notation.

For example, if you want to import the `sqrt` function from the `math` module, you can use the following statement:

```python
from math import sqrt
```

# Advantages

Using the `import module` statement has the advantage of making all the module’s contents available in the current namespace. This can be useful when you need to access multiple functions or attributes from the same module.

Using the `from module import` statement has the advantage of making specific functions or attributes available without having to use dot notation. This can make your code easier to read and understand.

# Disadvantages

Using the `import module` statement can lead to namespace conflicts if multiple modules have functions or attributes with the same name.

Using the `from module import` statement can lead to ambiguity if you are not careful with your imports. For example, if you import two functions with the same name from two different modules, you may not be able to tell which one you are using.
