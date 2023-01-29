---
title: What is the best way to end a script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To terminate a script in Python, use the exit() or quit() functions.
---

**Contents**

[TOC]

# Using sys.exit()
The sys.exit() method can be used to terminate a script in Python. This method takes an optional argument which is the exit code. If no argument is provided, the exit code is assumed to be 0, indicating successful termination.

# Using os._exit()
The os._exit() method can also be used to terminate a script in Python. Unlike the sys.exit() method, this method does not take any arguments and immediately terminates the script without any cleanup operations.

# Using raise SystemExit
The SystemExit exception can also be used to terminate a script in Python. This can be done by raising the SystemExit exception using the raise keyword. This method also takes an optional argument which is the exit code. If no argument is provided, the exit code is assumed to be 0, indicating successful termination.
