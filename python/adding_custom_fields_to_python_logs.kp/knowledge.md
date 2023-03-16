---
title: What is the process to include a personalized field in the string format of Python logs?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the %(fieldname)s syntax to include the custom field name in the log format string and pass the field as a parameter to the logger call.
---

**Contents**

[TOC]

## Section 1: Introduction

Logging is a crucial aspect of software development. It helps developers diagnose issues or errors that arise in the code. Python provides an inbuilt module, logging, to facilitate logging in Python applications. The logging module comes with a set of built-in loggers, handlers, filters, and formatters, which can be configured as per the requirements. In this tutorial, we will learn how to add a custom field to the Python log format string.

## Section 2: Understanding Python Log Format String

Python logging module's Formatter class formats the logs based on a string passed as the argument log format string. The log format string specifies the structure of the log message that will be generated. The Formatter class uses string placeholders to replace with appropriate log messages. For example, you can use '%(asctime)s - %(levelname)s - %(message)s' as a log format string, where %(asctime)s, %(levelname)s, and %(message)s are placeholders.

## Section 3: Adding a Custom Field to the Python Log Format String

To add a custom field to the Python log format string, you can use the extra parameter of the Logger method to pass any extra data alongside the log record. The extra data should be passed as a dictionary, where each key-value pair represents the key-value pair of the extra field. You can then use the extra field's key inside the log format string's placeholders to create a custom log.

For example:

```python
import logging

logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(levelname)s - %(message)s - %(custom_field)s')
logger = logging.getLogger()

extra = {'custom_field': 'custom_value'}

logger.debug('This is a debug log', extra=extra)
```

Output:

```
2021-10-27 15:40:52,297 - DEBUG - This is a debug log - custom_value
```

Here, we added a custom_field to the log format string by constructing an extra dictionary and passing the log extra parameter with the logger method.

## Section 4: Conclusion

In this tutorial, we learned how to add a custom field to the Python log format string. We saw that we can use the extra parameter of the logger method to pass the additional data, which can then be referred to within the logging format string. This can be useful to supplement the log messages with additional context or metadata, as specified by the developer's requirements.
