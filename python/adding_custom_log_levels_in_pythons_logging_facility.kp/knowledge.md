---
title: Ways to incorporate a personalized log level into the logging mechanism of python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To add a custom loglevel to Python`s logging facility, you need to define it using the `addLevelName()` method and assign a numeric value to it.
---

**Contents**

[TOC]

## Introduction

Python's logging facility is a powerful tool for capturing and analyzing application logs. It provides various facilities for logging messages at different levels, such as `DEBUG`, `INFO`, `WARNING`, `ERROR` and `CRITICAL`. However, there is often a need to define additional custom log levels that can help in better organizing and prioritizing log messages. In this article, we will discuss how to add a custom loglevel to Python's logging facility.

## Step 1: Define the log level

The first step in adding a custom log level is to define it. Custom log levels are represented as integers, and their values should be unique and higher than that of the highest built-in log level (`CRITICAL` in this case). For example, if we want to define a new log level called `VERBOSE`, we can define it as follows:

```python
import logging
VERBOSE = logging.DEBUG - 1
logging.addLevelName(VERBOSE, "VERBOSE")
```

Here, we have defined `VERBOSE` as an integer value one less than `DEBUG` and used the `addLevelName()` method to associate it with the name "VERBOSE". This ensures that the log messages with this level will have the correct name when displayed in logs.

## Step 2: Add a custom log method

Once we have defined our custom log level, we need to add a custom logging method that can be used to log messages at this level. The logging module provides the `LoggerAdapter` class, which can be used to add custom methods to a logger instance. For example, we can add a custom method called `verbose()` to our logger:

```python
class VerboseLoggerAdapter(logging.LoggerAdapter):
    def verbose(self, msg, *args, **kwargs):
        self.log(VERBOSE, msg, *args, **kwargs)

logger = logging.getLogger(__name__)
logger = VerboseLoggerAdapter(logger, {})
```

Here, we have created a new class called `VerboseLoggerAdapter` that inherits from `logging.LoggerAdapter`. We then define a custom method called `verbose()` that calls the `log()` method with our custom log level (`VERBOSE`) and the message to be logged. Finally, we create an instance of `VerboseLoggerAdapter` by passing our logger instance and an empty dictionary to its constructor. This will ensure that our custom method is added to the logger and can be used for logging messages at the custom log level.

## Step 3: Use the custom method to log messages

Once we have added the custom method to our logger, we can use it to log messages at our custom log level. For example:

```python
logger.verbose("This is a verbose message")
```

Here, we are calling the `verbose()` method to log a message at our custom log level. This message will be displayed in logs along with its custom log level name ("VERBOSE").

## Conclusion

In this article, we discussed how to add a custom log level to Python's logging facility. We saw how to define the log level, add a custom logging method to a logger, and use the custom method to log messages. Custom log levels can be useful in organizing and prioritizing log messages, and Python's logging facility provides a flexible and extensible framework for working with them.
