---
title: The name of the Python script and the line number
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The filename and line number of a Python script can be displayed in error messages and stack traces to help identify the source of the error.
---

**Contents**

[TOC]

Getting the filename and line number of a Python script

To get the filename and line number of a Python script, you can make use of traceback module in Python. The traceback module provides a way to output error message and traceback details. It also has some handy functions for inspecting the current program state and retrieving information about the active interpreter stack.

1. The traceback module

The traceback module can be imported using the `import traceback` statement. This module provides a function called `print_exc()` that prints the traceback of the last exception that occurred in the program.

2. Getting the filename and line number

To get the filename and line number of a Python script, you can make use of the `sys.exc_info()` function. This function returns a tuple containing information about the most recent exception that occurred in the Python interpreter.

Here's a sample code that demonstrates how to get the filename and line number of a Python script:

```python
import traceback
import sys

try:
    # Some code that may raise an exception
    ...
except:
    exc_type, exc_value, exc_traceback = sys.exc_info()
    tb_lines = traceback.format_tb(exc_traceback)
    print(tb_lines[-1])  # Print the last traceback entry
```

In the above code, we first import the traceback and sys modules. We then wrap our code in a try-except block to catch any exceptions that may occur. If an exception is caught, we use the `sys.exc_info()` function to retrieve information about the exception. We then use the `traceback.format_tb()` function to format the traceback into a list of strings. Finally, we print the last traceback entry in the list, which contains the filename and line number of the code that raised the exception.

3. Using the inspect module

Another way to get the filename and line number of a Python script is by using the inspect module. This module provides several functions for inspecting the properties of live objects and retrieving information about the source code of modules, functions, and classes.

Here's a sample code that demonstrates how to get the filename and line number of a Python script using the inspect module:

```python
import inspect

def some_function():
    frame_info = inspect.getframeinfo(inspect.currentframe())
    print(frame_info.filename, frame_info.lineno)

# Call the function
some_function()
```

In the above code, we first import the inspect module. We then define a function called `some_function()`, which uses the `inspect.getframeinfo()` function to retrieve information about the current frame. The `inspect.currentframe()` function returns the frame object that represents the current execution frame. We then use the `frame_info.filename` and `frame_info.lineno` attributes to print the filename and line number of the current frame.

Conclusion

In summary, you can get the filename and line number of a Python script by using either the traceback module or the inspect module. The traceback module provides a simple way to print the traceback of the last exception that occurred in the program, while the inspect module provides more fine-grained control over the inspection of live objects and source code.
