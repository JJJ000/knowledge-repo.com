---
title: Creating private functions in a Python module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Private module functions in Python are functions that are visible and accessible only within the module in which they are defined.
---

**Contents**

[TOC]

# Section 1: Introduction

Private module functions are functions that are not accessible from outside the module they are defined in. They are typically used to hide implementation details from the user, allowing them to focus on the interface of the module. In Python, private module functions are indicated by a leading underscore in the function name.

# Section 2: Syntax

Private module functions are declared in the same way as regular functions, with the only difference being the leading underscore in the function name. For example:

```
def _private_function():
    # code here
```

# Section 3: Accessibility

Private module functions are not accessible from outside the module they are defined in. They can only be called from within the module itself, or from other functions defined in the same module.

# Section 4: Benefits

Private module functions can be useful for hiding implementation details from the user of the module, allowing them to focus on the interface of the module. They can also help to reduce the complexity of the module, making it easier to maintain and debug.
