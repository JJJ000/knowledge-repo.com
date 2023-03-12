---
title: Retrieve traceback information from an object representing an exception
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the traceback module to extract traceback information from an exception object in Python.
---

**Contents**

[TOC]

### Introduction

In Python, when an error or exception occurs, the interpreter raises an exception object that contains information about the error. This information is referred to as the traceback information. Extracting this information is helpful in debugging the code and understanding the source of the error. In this article, we will see how to extract traceback info from an exception object in Python.


### Using traceback module

Python provides a built-in module called traceback that can be used to extract the traceback information from an exception object. The traceback module provides methods for formatting and printing the traceback information in various formats.

```python
import traceback

try:
    # code that generates an exception
except Exception as e:
    traceback.print_tb(e.__traceback__)
```

In the above code snippet, we are printing the traceback information by calling the print_tb method of the traceback module and passing the traceback object obtained from the exception object.


### Using sys module

Python's built-in sys module provides another way of accessing the traceback object. We can use the sys module to get the traceback object and further process it to obtain the traceback information.

```python
import sys

try:
    # code that generates an exception
except Exception as e:
    exc_type, exc_value, exc_traceback = sys.exc_info()
    traceback.print_tb(exc_traceback)
```

In the above code example, we are obtaining the traceback object using the sys.exc_info() method and further processing it to obtain the traceback information.


### Accessing individual traceback frames

Both the traceback module and sys module provide ways of accessing individual traceback frames. We can iterate over the frames to obtain information about each frame.

```python
import traceback

try:
    # code that generates an exception
except Exception as e:
    for tb in traceback.walk_tb(e.__traceback__):
        filename = tb.tb_frame.f_code.co_filename
        line_no = tb.tb_lineno
        function_name = tb.tb_frame.f_code.co_name
        print(f"{filename}:{line_no} {function_name}")
```

In the above code, we are iterating over the traceback frames by calling the walk_tb method of the traceback module and accessing the frame attributes to obtain information about each frame.

### Conclusion

In conclusion, extracting traceback info from an exception object in Python is essential in debugging the code and understanding the source of the error. We can use the traceback module and sys module to obtain the traceback object and further process it to obtain the traceback information. We can also access the individual traceback frames to obtain more detailed information about each frame.
