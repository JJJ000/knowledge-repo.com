---
title: How to log Python functions, file names, and line numbers using a single file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: By defining a Formatter with format string that includes %(funcName)s, %(filename)s, and %(lineno)d, and setting it to the root logger`s handler, the Python logging module can be used to log function name, file name, and line number using a single file.
---

**Contents**

[TOC]

Section 1: Introduction to Python Logging
Python logging is the process of tracking events that happen when software runs. Logging is important for software development as it provides a way to diagnose and fix issues. It also provides valuable information to software maintainers and administrators. Python logging can be done using the built-in logging module.

Section 2: Adding Function Name, File Name, and Line Number to Logging Output
To add function name, file name, and line number to the logging output, we need to use the format attribute of the logging module. Here’s an example:

```python
import logging

logging.basicConfig(format='%(asctime)s: %(levelname)s: %(funcName)s:%(filename)s:%(lineno)d: %(message)s',level=logging.DEBUG)

def myFunction():
    logging.debug("Debug message from %s function in file %s on line %s",myFunction.__name__,__file__,__lineno__)

myFunction()
```

In the above example, we have used the basicConfig() function to configure logging. Here, we have set the format attribute to include the function name, file name, and line number.

Section 3: Using a Single Configuration File for Logging
To use a single configuration file for logging, we can create a logging.ini or logging.conf file and specify the settings for logging in this file. Here’s an example of how the logging.ini file may look like:

```ini
[loggers]
keys=root

[handlers]
keys=consoleHandler

[formatters]
keys=myFormatter

[logger_root]
level=DEBUG
handlers=consoleHandler

[handler_consoleHandler]
class=StreamHandler
level=DEBUG
formatter=myFormatter
args=(sys.stdout,)

[formatter_myFormatter]
format=%(asctime)s: %(levelname)s: %(funcName)s:%(filename)s:%(lineno)d: %(message)s
datefmt=%Y-%m-%d %H:%M:%S
```

In the above example, we have defined the settings for logging in the logging.ini file. We have specified the loggers, handlers, and formatters keys. We have also defined the format for logging, which includes the function name, file name, and line number.

Section 4: Using the Configuration File in Python Code
To use the configuration file in Python code, we need to use the fileConfig() function of the logging module. Here’s an example:

```python
import logging
import logging.config

logging.config.fileConfig('logging.ini')

def myFunction():
    logging.debug("Debug message from %s function in file %s on line %s",myFunction.__name__,__file__,__lineno__)

myFunction()
```

In the above example, we have used the fileConfig() function to read the logging settings from the logging.ini file. We have then used the logging.debug() function to log the message, which includes the function name, file name, and line number.
