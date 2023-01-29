---
title: What is the best way to capture and display the full exception traceback without stopping the program from running?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `traceback` module to print the full exception traceback without halting/exiting the program.
---

**Contents**

[TOC]

## Using Try/Except

Python provides the `try` and `except` keywords to handle exceptions.

```python
try:
    # code to be executed
except Exception as e:
    # code to execute if exception occurs
    print(e)
    traceback.print_exc()
```

The `except` clause can be used to catch any exception, and the `e` variable stores the exception object. The `print()` function can be used to print the exception object, and the `traceback.print_exc()` function can be used to print the full traceback.

## Using Logging

Python's `logging` module can also be used to capture and print the full traceback.

```python
import logging

logging.basicConfig(level=logging.DEBUG)

try:
    # code to be executed
except Exception as e:
    # code to execute if exception occurs
    logging.exception(e)
```

The `logging.basicConfig()` function can be used to configure the logging module. The `level` argument can be set to `logging.DEBUG` to enable debug logging. The `logging.exception()` function can then be used to log the exception and print the full traceback.
