---
title: What is the path of a module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The path of a module can be retrieved using the built-in function \_\_file\_\_.
---

**Contents**

[TOC]

# Section 1: Using the __file__ Attribute

The `__file__` attribute of a module can be used to retrieve the absolute path of the module.

# Section 2: Example

For example, if we have a module called `my_module.py` located in the directory `/home/user/my_modules`, the following code can be used to retrieve the absolute path of the module:

```python
import my_module

print(my_module.__file__)
```

This will output `/home/user/my_modules/my_module.py`.

# Section 3: Using the Pathlib Module

The `Pathlib` module can also be used to retrieve the absolute path of a module.

# Section 4: Example

For example, if we have a module called `my_module.py` located in the directory `/home/user/my_modules`, the following code can be used to retrieve the absolute path of the module:

```python
from pathlib import Path
import my_module

print(Path(my_module.__file__).resolve())
```

This will output `/home/user/my_modules/my_module.py`.
