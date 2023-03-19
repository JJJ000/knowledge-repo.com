---
title: How to format time in Python logging to include milliseconds?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, you can use milliseconds in the time format for Python logging by including `%f` in the date format argument.
---

**Contents**

[TOC]

1. Introduction
In Python, logging is a built-in module that allows developers to track and record the activity of their application. One of the commonly used features of logging is the ability to customize the time format. In this article, we will discuss how to use milliseconds in time format.

2. Default time format
By default, the logging module uses the time format '%(asctime)s'. This format displays the timestamp in the format 'YYYY-MM-DD HH:MM:SS,sss', where 'sss' represents milliseconds. However, the default value of milliseconds is always '000'.

3. Using milliseconds in time format
To include milliseconds in the time format, you need to modify the format string to include the millisecond value. The complete format string for the timestamp with milliseconds is '%(asctime)s,%(msecs)d'. The '%(msecs)d' denotes the millisecond value as a decimal integer.

Here's an example:

```
import logging

logging.basicConfig(format='%(asctime)s,%(msecs)d %(levelname)-8s [%(filename)s:%(lineno)d] %(message)s',
                    datefmt='%Y-%m-%d:%H:%M:%S')

logger = logging.getLogger('test')
logger.setLevel(logging.DEBUG)

logger.debug('This is a debug message')
```

This will output the following log message:
```
2021-10-25 10:27:56,776 DEBUG   [example.py:9] This is a debug message
```

4. Conclusion
In this article, we have discussed how to use milliseconds in the Python logging module's time format. By modifying the format string, we can include milliseconds in the timestamp. This can be useful for debugging and performance analysis in production environments.
