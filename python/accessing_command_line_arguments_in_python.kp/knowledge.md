---
title: What is the procedure for accessing command line arguments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Command line arguments can be accessed using the sys.argv list.
---

**Contents**

[TOC]

#1 Accessing Command Line Arguments

Python provides access to command line arguments through the `sys` module. To access the arguments, use `sys.argv` which is a list containing the arguments passed to the script.

#2 Parsing Command Line Arguments

The `sys.argv` list can be used to parse command line arguments. By looping through the list, you can determine the type of argument and the value of that argument.

#3 Argument Parsing Libraries

There are several argument parsing libraries available for Python, such as `argparse`, `docopt` and `optparse`. These libraries provide more advanced argument parsing capabilities and are recommended for complex command line argument processing.

#4 Example

The following example shows how to access and parse command line arguments using the `sys` module:

```python
import sys

for arg in sys.argv:
    if arg.startswith('--'):
        # argument is a flag
    elif arg.startswith('-'):
        # argument is an option
    else:
        # argument is a value
```
