---
title: How can global variables be shared between different files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Global variables can be shared between files in Python by importing the file containing the global variable.
---

**Contents**

[TOC]

**Section 1: Introduction**

Global variables are variables that are declared outside of a function and can be accessed by any function in the program. In Python, global variables are declared using the keyword “global”. Global variables can be used to share data between different files in a Python program.

**Section 2: Declaration**

To declare a global variable in Python, the keyword “global” must be used. The variable name should then be provided. For example:

```
global my_variable
```

**Section 3: Accessing Global Variables**

To access a global variable from another file, the keyword “global” must be used again. The variable name should then be provided. For example:

```
global my_variable
my_variable = 10
```

**Section 4: Conclusion**

Global variables can be used to share data between different files in a Python program. To declare a global variable, the keyword “global” must be used. To access a global variable from another file, the keyword “global” must be used again.
