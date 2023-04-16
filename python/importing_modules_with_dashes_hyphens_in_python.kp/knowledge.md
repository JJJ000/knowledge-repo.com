---
title: How can I import a module when the module name contains a hyphen?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can import a module with a hyphen in its name by using the `from` keyword and surrounding the module name with quotes.
---

**Contents**

[TOC]

# Using importlib

The importlib module provides an API for importing Python modules. It can be used to import modules with hyphens in their names.

## Steps
1. Import the importlib module.

```
import importlib
```

2. Use the import_module() method to import the module.

```
module_name = 'module-name'
module = importlib.import_module(module_name)
```

# Using __import__

The __import__() function can also be used to import modules with hyphens in their names.

## Steps
1. Use the __import__() function to import the module.

```
module_name = 'module-name'
module = __import__(module_name)
```

2. Access the module's attributes and methods.

```
module.some_attribute
module.some_method()
```
