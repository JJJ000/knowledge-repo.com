---
title: Is it possible to create aliases for imported modules in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can define aliases for imported modules in Python using the `as` keyword.
---

**Contents**

[TOC]

# Overview of Aliasing Modules in Python

In Python, it is possible to alias imported modules by assigning a different name to them while importing. This is useful when the name of the module is too long or when we want to avoid name conflicts with other modules or variables in the code.

There are two commonly used ways to alias modules in Python:

1. Using the `import module as alias` syntax
2. Using the `from module import *` syntax and specifying the module name as an alias

In the following sections, we will explore each of these methods in more detail.

# Aliasing Modules using `import module as alias`

To alias a module using the `import module as alias` syntax, we simply replace `module` with the name of the module we want to import, and `alias` with the name we want to use as an alias.

Here's an example:

```python
import numpy as np

# Using the numpy module with its alias `np`
a = np.array([1, 2, 3])
print(a)
```

In this example, we're importing the `numpy` module and giving it the alias `np`. This allows us to use the `numpy` module under the shorter name `np`.

# Aliasing Modules using `from module import *` and specifying an alias

Another way to alias a module is by using the `from module import *` syntax, and specifying an alias for the module.

Here's an example:

```python
from numpy import * as np

# Using the numpy module with its alias `np`
a = np.array([1, 2, 3])
print(a)
```

In this example, we're using the `from numpy import *` syntax to import all the functions and objects from the `numpy` module, and then specifying the name `np` as an alias for the entire module.

Note that this method is not recommended, as it can lead to naming conflicts and make it difficult to identify where objects are coming from in the code. It's generally better to use the `import module as alias` syntax when aliasing modules in Python.

# Conclusion

Aliasing modules in Python can be a useful technique for making code more readable and avoiding name collisions. In this article, we covered two commonly used methods for aliasing modules in Python: using the `import module as alias` syntax and using the `from module import *` syntax and specifying an alias. Remember to use aliasing carefully, and to choose clear and descriptive names for your aliases.
