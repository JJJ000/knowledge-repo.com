---
title: What is the process to turn off logging on the standard error stream?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Add `stderr=None` as a parameter when calling the Python script.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, logging is a powerful tool that allows developers to record information about their applications. It allows them to see what is happening within the application, troubleshoot issues, and optimize performance. However, sometimes logging can become too verbose, and users may prefer to turn off specific logs to reduce output noise.

Section 2: The logging module in Python
The logging module in Python is used to log messages from the application. The module provides the following logging levels:
```
CRITICAL
ERROR
WARNING
INFO
DEBUG
NOTSET
```
Each log message has a corresponding level, and developers can set a minimum level of messages they want to see. For example, if the minimum level is set to `INFO`, only messages with a level of `INFO` or above will be displayed.

Section 3: Disabling logging on the standard error stream
To disable logging on the standard error stream in Python, developers need to modify the logging handlers. The standard error stream is handled by the `StreamHandler` class. To disable logging on the standard error stream, developers need to remove the `StreamHandler` from the logger.

Here is an example:
```python
import logging
import sys

logger = logging.getLogger(__name__)

# Remove the StreamHandler from the logger
for handler in logger.handlers:
    if isinstance(handler, logging.StreamHandler) and handler.stream == sys.stderr:
        logger.removeHandler(handler)

# logging messages will no longer be displayed on the standard error stream
```

The code above checks if there is a `StreamHandler` object attached to the logger instance and removes it if it exists. Once the `StreamHandler` is removed, all log messages will no longer be displayed on the standard error stream.

Note that this will only remove the `StreamHandler` that is sending messages to the standard error stream. If there are other handlers that are sending messages to other destinations (e.g., a file), those handlers will still be active.

Section 4: Conclusion
In conclusion, disabling logging on the standard error stream can help reduce the amount of noise in the application output. Developers can achieve this by removing the `StreamHandler` object that is sending messages to the standard error stream.
