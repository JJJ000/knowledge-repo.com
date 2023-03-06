---
title: What occurs in Python when importing is done inside a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: When you import inside of a function, the module is still only loaded once into memory and subsequent imports simply reference the previously loaded module.
---

**Contents**

[TOC]

Scope of a function

In Python, a function creates a local scope for itself. This means that any variables or functions created within the function are only accessible within the function's scope.

Import statement

An import statement in Python is used to import a module or a specific component of a module. When the interpreter encounters an import statement, it searches for the module or component in the directories listed in the sys.path variable.

Import inside a function

When an import statement is used inside a function in Python, it is executed every time the function is called. This means that the module or component is loaded and initialized every time the function is called.

Implications of importing inside a function

Importing inside a function can have performance implications because the module or component is reloaded every time the function is called. It can also lead to namespace pollution because the module or component becomes part of the function's local namespace, which can cause conflicts with other variables or functions in the same namespace. 

In summary, importing inside a function in Python is allowed, but it can have performance and namespace implications. It is generally recommended to import modules and components at the top of a file, outside of any functions, to avoid these issues.
