---
title: What are the steps to record the name and line number of the source file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the built-in logging module with a custom formatter that includes the source file name and line number.
---

**Contents**

[TOC]

## Use of traceback module

```python
import traceback

try:
    # Your code here
except Exception as e:
    print(traceback.format_exc())
```

The `traceback` module provides a function `format_exc()` that will return a formatted string which contains the traceback of the current exception. This includes the source file name and line number of each line of code that is executed before the exception occurred. In the above code snippet, we are catching any exception that occurs and printing out the traceback using `format_exc()`.


## Using the logging module

```python
import logging

logging.basicConfig(filename='example.log', level=logging.DEBUG)

try:
    # Your code here
except Exception as e:
    logging.exception("Error occurred")
```

The `logging` module provides a way to write log messages from your Python application. By default, the logging module does not include the source file name and line number of each log message. However, you can include this information by specifying the `exc_info=True` parameter in the logging message. By doing this, the logging module will automatically include the traceback information, which includes the source file name and line number. In the above code snippet, we are catching any exception that occurs and logging the error message along with the traceback information using `logging.exception()`.


## Using the inspect module

```python
import inspect

def function_name():
    # Your code here
    for frame_record in inspect.stack():
        filename, line_num, function_name, line_of_code, index = frame_record
        print(f"File Name: {filename},\nLine number: {line_num}")

function_name()
```

The `inspect` module provides functions to retrieve information about the current stack frame, which includes the current source file name and line number. You can use the `inspect.stack()` function to retrieve the current stack frame and iterate over the returned list of frame records to obtain the source file name and line number for each frame. In the above code snippet, we define a function `function_name()` which contains the code to be executed. We then retrieve the stack frame using `inspect.stack()` and iterate over the frame records to retrieve the source file name and line number for each frame.


## Using the linecache module

```python
import linecache

filename = './your_file_name.py'
line_num = 10
line_text = linecache.getline(filename, line_num)

print(f"File Name: {filename},\nLine number: {line_num},\nLine Text: {line_text}")
```

The `linecache` module provides a way to retrieve lines of text from a file. You can use the `getline()` function to retrieve the line of text from a specific line number in a file. By specifying the source file name and line number, you can retrieve the line of code that was executed when an exception occurred. In the above code snippet, we retrieve line number 10 from the file "your_file_name.py" and print out the source file name, line number and line text.
