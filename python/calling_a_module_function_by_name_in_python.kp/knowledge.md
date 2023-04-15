---
title: Invoking a function of a module by its name (a string)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can call a function of a module by using its name as a string with the built-in function getattr().
---

**Contents**

[TOC]

## Import Module

In order to call a function of a module by using its name in Python, the module must first be imported. This is done using the `import` statement. For example, to import the `math` module:

```python
import math
```

## Get Function Name

Once the module is imported, the function name can be obtained as a string. This can be done by accessing the module's `__name__` attribute. For example, to get the name of the `sqrt` function from the `math` module:

```python
func_name = math.sqrt.__name__
```

This will set `func_name` to the string `"sqrt"`.

## Call Function

Once the function name is obtained as a string, it can be used to call the function. This is done using the `getattr` function. This function takes two arguments: the module and the name of the function to call. For example, to call the `sqrt` function from the `math` module:

```python
result = getattr(math, func_name)(4)
```

This will set `result` to the value `2.0`.

## Summary

In summary, to call a function of a module by using its name in Python, the module must first be imported. Then, the function name can be obtained as a string by accessing the module's `__name__` attribute. Finally, the function can be called using the `getattr` function.
