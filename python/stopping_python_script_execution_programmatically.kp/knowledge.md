---
title: How do you halt the execution of a Python script using code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To programmatically stop execution of a Python script, use the `sys.exit()` function or a try-except block with a `KeyboardInterrupt` exception.
---

**Contents**

[TOC]

There are several ways to programmatically stop the execution of a Python script. Here are a few options:

## Using sys.exit()

The `sys.exit()` function is a convenient way to immediately terminate the script execution. When this function is called, the Python interpreter raises the `SystemExit` exception, which can be caught and handled if necessary. Here's an example:

```python
import sys

# exit the script with a status code of 0 (success)
sys.exit(0)

# exit with a non-zero status code (failure)
sys.exit(1)
```

## Using os._exit()

The `os._exit()` function is similar to `sys.exit()`, but it immediately terminates the Python interpreter without performing any cleanup or running any cleanup handlers. This can be useful if you need to terminate the script in the middle of an operation that cannot be interrupted or undone. Here's an example:

```python
import os

# exit immediately with a status code of 0
os._exit(0)

# exit immediately with a non-zero status code
os._exit(1)
```

## Using a custom exception

You can define your custom exception class and raise an instance of it to stop the script execution. This approach can be useful if you need to handle the exception in a specific way or collect additional information about the error before terminating the script. Here's an example:

```python
class MyCustomError(Exception):
    pass

# raise the custom exception to stop the script
raise MyCustomError("Something went wrong")
```

## Using KeyboardInterrupt

The `KeyboardInterrupt` exception is raised when the user presses Ctrl+C or sends a SIGINT signal to the Python interpreter. You can catch this exception to gracefully stop the script execution and perform any necessary cleanup. Here's an example:

```python
try:
    while True:
        # do some work here
        pass
except KeyboardInterrupt:
    # stop the script gracefully on Ctrl+C
    print("User interrupted the script")
```
