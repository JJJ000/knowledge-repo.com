---
title: Reload a module while in an interactive session
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the reload() function to reimport a module while interactive in Python.
---

**Contents**

[TOC]

# Section 1: Import Module

In order to reimport a module while interactive in Python, we must first import the module. This can be done using the `import` statement.

```python
import module_name
```

# Section 2: Reload Module

Once the module has been imported, it can be reloaded using the `reload` function from the `importlib` module.

```python
from importlib import reload
reload(module_name)
```

# Section 3: Check Reload

To ensure that the module was successfully reloaded, we can check the version of the module using the `version` attribute.

```python
module_name.version
```

# Section 4: Confirm Reload

Finally, we can confirm the reload of the module by running some of its functions or classes.

```python
module_name.function_name()
```
