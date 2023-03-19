---
title: How can I use setattr() on the module I am currently working on?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the built-in function `setattr()` and pass `sys.modules[\_\_name\_\_]` as the first argument.
---

**Contents**

[TOC]

## Getting the Current Module

In order to call `setattr()` on the current module in Python, we must first retrieve the current module. We can do this by using the special built-in variable `__name__`, which contains the name of the current module as a string.

```python
import sys

current_module = sys.modules[__name__]
```

Here, we use the `sys.modules` dictionary to retrieve the current module by name. We use `__name__` to get the name of the current module as a string, which we pass as a key to `sys.modules`. The result is the current module object, which we assign to the variable `current_module`.


## Setting an Attribute with setattr()

Now that we have the current module, we can call `setattr()` to set an attribute on the module. `setattr()` takes three arguments: the object to set the attribute on, the name of the attribute as a string, and the value to set the attribute to.

```python
setattr(current_module, 'my_attribute', 42)
```

Here, we call `setattr()` on the `current_module` object and pass `'my_attribute'` as the name of the attribute we want to set. We set the attribute to the value `42`, but this could be any value of any type.


## Example: Setting Multiple Attributes

Let's say we want to set multiple attributes on the current module at once. We can do this by using a loop and a dictionary of attribute names and values.

```python
attributes = {
    'my_attribute': 42,
    'my_other_attribute': 'hello',
    'my_third_attribute': [1, 2, 3]
}

for name, value in attributes.items():
    setattr(current_module, name, value)
```

Here, we define a dictionary called `attributes` that contains three items, each representing an attribute name and value to set on the current module. We then use a loop to iterate over the items in the dictionary, calling `setattr()` for each name and value.

The end result is that the current module will have three new attributes:

```python
print(my_attribute)            # 42
print(my_other_attribute)      # 'hello'
print(my_third_attribute)      # [1, 2, 3]
```
