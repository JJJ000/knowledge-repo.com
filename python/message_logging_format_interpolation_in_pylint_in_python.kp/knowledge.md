---
title: This is a pylint notification regarding the interpolation of logging formats
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: PyLint message `logging-format-interpolation` indicates that string formatting using %-style interpolation should be replaced with f-strings or str.format() method.
---

**Contents**

[TOC]

Section 1: Explanation of PyLint and logging-format-interpolation

PyLint is a widely used tool for analyzing source code and finding errors and bugs in Python programming language. It is considered a powerful static analysis tool because it can detect issues before the code is executed. One of the issues that PyLint can detect is related to the logging module in Python. In particular, PyLint can flag code that uses old-style string formatting with the logging module instead of using the newer format strings. This issue is known as 'logging-format-interpolation'.

Section 2: Issue with old-style string formatting

Old-style string formatting with the logging module can lead to issues such as missing or misplaced parameters, which can cause confusion and errors in the code. For example, consider the following code:

```
import logging
logging.basicConfig(level=logging.INFO,
                    format='%(asctime)s %(levelname)s %(message)s',
                    datefmt='%Y-%m-%d %H:%M:%S')
name = 'Bob'
logging.info('Hello %s', name)
```

In this code, the logging module is using old-style string formatting by using `%s` to insert the `name` variable into the log message. This can be problematic if the message contains more than one `%s` and the order is not correct.

Section 3: New-style string formatting with f-strings

To avoid the issue of old-style string formatting, PyLint recommends using new-style string formatting with f-strings. F-strings were introduced in Python 3.6 and provide a simpler and more intuitive way of formatting strings. Using f-strings in the previous example, the code would look like this:

```
import logging
logging.basicConfig(level=logging.INFO,
                    format='%(asctime)s %(levelname)s %(message)s',
                    datefmt='%Y-%m-%d %H:%M:%S')
name = 'Bob'
logging.info(f'Hello {name}')
```

In this example, the `f` prefix is used to indicate that the string is a f-string. The `name` variable is enclosed in curly braces `{}` which denotes the placeholder for the variable in the message.

Section 4: Conclusion

In conclusion, PyLint's 'logging-format-interpolation' issue is related to the use of old-style string formatting with the logging module in Python. This can lead to issues such as misplaced or missing parameters. PyLint recommends using new-style string formatting with f-strings as a solution. F-strings provide a simpler and more intuitive way of formatting strings and are available from Python 3.6 onwards.
