---
title: What is the process for obtaining the type, file, and line number when I encounter an exception?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the built-in functions `type`, `\_\_file\_\_`, and `\_\_line\_\_` to get the type, file, and line number of an exception in Python.
---

**Contents**

[TOC]

## Using sys.exc_info()

The `sys.exc_info()` function returns a tuple containing information about the most recent exception that has occurred. This tuple contains three values: the type of exception that occurred, the value of the exception, and a traceback object. The traceback object contains information about the file and line number where the exception occurred.

## Accessing the Traceback Object

Once the tuple is returned from `sys.exc_info()`, the traceback object can be accessed by indexing the tuple. The traceback object contains all of the information needed to get the type, file, and line number of the exception.

## Extracting the Information

Once the traceback object is accessed, the `tb_lineno` attribute can be used to get the line number where the exception occurred. The `tb_frame` attribute can be used to get the frame object, which contains the file name and the name of the function in which the exception occurred. Finally, the type of exception can be extracted from the tuple returned by `sys.exc_info()`.

## Example

Here is an example of how to extract the type, file, and line number of an exception using `sys.exc_info()`:

```python
try:
    # some code
except Exception as e:
    exc_type, exc_value, exc_traceback = sys.exc_info()
    line_number = exc_traceback.tb_lineno
    file_name = exc_traceback.tb_frame.f_code.co_filename
    exception_type = exc_type
```
