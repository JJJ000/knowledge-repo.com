---
title: Re-wording 'sibling package imports'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Package imports in Python allow you to import modules from other packages in the same directory.
---

**Contents**

[TOC]

# Section 1: What are Sibling Package Imports?
Sibling package imports are a type of import in Python that allow you to import modules from the same package. This type of import is useful when you need to access modules in the same package but in different directories.

# Section 2: How to Use Sibling Package Imports
Sibling package imports are used by adding the relative path from the current module to the module you want to import. This is done by using the `from` keyword followed by the relative path to the module you want to import.

# Section 3: When to Use Sibling Package Imports
Sibling package imports are useful when you need to access modules in the same package but in different directories. This type of import is also useful when you need to access modules from different packages that have the same name.

# Section 4: Example
For example, if you have a module called `my_module.py` in the package `my_package`, you can use a sibling package import to import another module in the same package, such as `my_other_module.py`. You would do this by using the following code:

```
from .my_other_module import *
```
