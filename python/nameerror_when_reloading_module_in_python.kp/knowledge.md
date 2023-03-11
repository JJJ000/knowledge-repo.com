---
title: The module reload is not defined, resulting in a nameerror when attempting to reload the module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: In Python 3, the built-in function reload() has been moved to the importlib module, so you need to import it from importlib and use it as importlib.reload().
---

**Contents**

[TOC]

Section: Overview
The NameError "name 'reload' is not defined" in Python is raised when you try to reload a module using the Python built-in reload function, but the function is not available or defined in your current version of Python. This error often occurs when you are using Python 3.x, which removed the reload function that was available in Python 2.x.


Section: Solutions
1. Use importlib module instead of reload: In Python 3, you can use the importlib module to dynamically load and reload modules. For instance, if you want to reload a module called my_module, you can use the following code:

```Python
import importlib
importlib.reload(my_module)
```

2. Import reload from the importlib module: If you prefer to keep using the reload function, you can also import it from the importlib module, which is available in both Python 2 and Python 3:

```Python
from importlib import reload
reload(my_module)
```

3. Use autoreload from IPython: If you are using IPython, you can also use the autoreload extension to automatically reload the modules every time they are modified. To enable the extension, use the following commands:

```Python
%load_ext autoreload
%autoreload 2
```

Section: Examples
Here is an example code snippet that shows how to reload a module using the importlib module:

```Python
import importlib
import my_module

# do some work with my_module...

# reload the module
importlib.reload(my_module)

# do some more work with my_module...
```

And here is an example code snippet that shows how to use the autoreload extension in IPython:

```Python
%load_ext autoreload
%autoreload 2

import my_module

# do some work with my_module...

# now suppose you modify the module code
# by adding some new functions or variables

# the modified module will be automatically reloaded
# when you execute the following statement
my_module.new_function()

# do some more work with my_module...
```
