---
title: The Python logging module is not producing any output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You need to configure a logging handler with a desired level and format in order to output logging messages.
---

**Contents**

[TOC]

## Introduction
Python logging is a module that allows developers to track events that occur when their code is executed. It is an essential tool for debugging Python code, as it enables us to monitor the behavior of our programs at runtime. However, sometimes the logging module might behave abnormally, and you might find that it is not outputting anything. In this article, we will discuss some common reasons why logging might fail to produce any output and how to fix them.

## Check logging level
One possible reason why logging might not be outputting anything is that the logging level is set too high. Each logging message has an associated level, and the logging module only outputs messages with levels that are equal to or higher than the current logging level. By default, the logging level is set to WARNING, which means that only messages of level WARNING or higher will be outputted. To change the logging level, you can use the `basicConfig()` function from the logging module. For example, to set the logging level to DEBUG, you can call the `basicConfig()` function like this:

```python
import logging

logging.basicConfig(level=logging.DEBUG)
```

## Check logging handlers
Another reason why logging might not be outputting anything is that there are no handlers attached to the logger. Handlers are objects that determine how log messages are outputted, and without them, the logging module has no way of knowing where to send the log messages. To add a handler to the logger, you can use the `addHandler()` function from the logging module. For example, to send log messages to the console, you can add a StreamHandler like this:

```python
import logging

logging.basicConfig(level=logging.DEBUG)
console_handler = logging.StreamHandler()
logging.getLogger().addHandler(console_handler)
```

## Check logging filters
Finally, logging might not be outputting anything if there are no filters attached to the logger. Filters are objects that allow you to selectively suppress or allow certain messages based on their attributes. By default, the logging module does not have any filters attached to the logger, so all log messages will be outputted. However, if there are filters attached to the logger, and none of them allow the log messages to pass, then no messages will be outputted. To add a filter to the logger, you can use the `addFilter()` function from the logging module. For example, to only output messages with a specific attribute, you can add a Filter like this:

```python
import logging

class CustomFilter(logging.Filter):
    def filter(self, record):
        return record.name == 'my_module'

logging.basicConfig(level=logging.DEBUG)
console_handler = logging.StreamHandler()
console_handler.addFilter(CustomFilter())
logging.getLogger().addHandler(console_handler)
```

## Conclusion
Logging is a crucial tool for debugging Python code, and understanding how to configure it properly is essential. By checking the logging level, handlers, and filters, you can ensure that your logging module is outputting the correct information to help you debug your code.
