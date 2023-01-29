---
title: What is the best way to clear the results of the print function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the flush keyword argument of the print() function, e.g. print(`Hello World`, flush=True).
---

**Contents**

[TOC]

# Section 1: Using flush()

The flush() function can be used to flush the output of the print function in Python. This function is available in the sys module. To use it, you must first import the sys module.

```
import sys

print("Hello World!")
sys.stdout.flush()
```

# Section 2: Using file parameter

The print function also has a file parameter which can be used to flush the output. By default, this parameter is set to sys.stdout, which is the standard output stream. To flush the output, you can set the file parameter to sys.stdout.flush.

```
print("Hello World!", file=sys.stdout.flush)
```

# Section 3: Using flush parameter

The print function also has a flush parameter which can be used to flush the output. By default, this parameter is set to False. To flush the output, you can set the flush parameter to True.

```
print("Hello World!", flush=True)
```

# Section 4: Using stdout.flush()

The sys.stdout.flush() function can also be used to flush the output of the print function in Python. This function flushes the output of the standard output stream, which is where the print function prints its output.

```
print("Hello World!")
sys.stdout.flush()
```
