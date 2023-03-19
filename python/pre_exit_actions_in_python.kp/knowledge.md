---
title: Performing an action prior to the termination of the program
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the atexit module to register functions to be called before program exit.
---

**Contents**

[TOC]

# Using the atexit module

The `atexit` module in Python provides a simple way to register functions that will be executed just before the program terminates. These functions are registered using the `register()` method of the module.

Here's an example:

```python
import atexit

def goodbye():
    print("Goodbye!")

atexit.register(goodbye)

# rest of the program goes here
```

In this example, the `goodbye()` function will be called just before the program exits. You can register multiple functions using `atexit.register()`.

# Using try-finally block

Another approach to doing something before program exit in Python is to use a `try-finally` block. You can put the code you want to execute before program exit in the `finally` block, which will always be executed whether or not the `try` block raises an exception.

Here's an example:

```python
try:
    # main program logic goes here
finally:
    # code to execute before program exit goes here
```

In this example, the `finally` block will always be executed before the program exits, even if an exception is raised in the `try` block.

# Using signal handlers

Python provides a way to register signal handlers that will be called when certain signals are received by the program. The `signal` module can be used to set up signal handlers.

Here's an example:

```python
import signal

def handler(signum, frame):
    print("Received signal {}".format(signum))

signal.signal(signal.SIGINT, handler)

# rest of the program goes here
```

In this example, the `handler()` function will be called when the program receives the `SIGINT` signal (which is sent when the user presses Control-C). You can register multiple signal handlers using the `signal.signal()` method. Note that some signals cannot be caught by Python programs (e.g. `SIGKILL`).
