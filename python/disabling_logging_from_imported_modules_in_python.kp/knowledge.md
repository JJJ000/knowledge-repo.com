---
title: How to turn off logging in imported modules using Python logging?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Set the logging level of the imported modules to a higher level than the root logger.
---

**Contents**

[TOC]

# Introduction 

Python logging is a powerful feature which allows developers to keep track of the processes and events occurring within an application in real-time. However, logging can get noisy when importing modules from external sources that generate their own logging messages. 

In this article, you'll learn how to disable logging from imported modules by configuring the logging settings appropriately.

# Disabling logging from imported modules

There are several ways to disable logging from imported modules. In this section, we will discuss the most common ways to do it. 

## 1. Disable logging by setting the logger level to CRITICAL

One way to disable logging from an imported module is to set the logger level to CRITICAL. By setting the logger level to CRITICAL, only messages with a severity of CRITICAL or higher will be logged. All other messages will be ignored. 

Here's an example of how to disable logging from an imported module using this technique:

```python
import logging
logging.getLogger("imported_module").setLevel(logging.CRITICAL)
```

In this example, the logger level for the "imported_module" logger is set to CRITICAL, which disables all messages except those with a severity level of CRITICAL or higher. 


## 2. Disable logging by creating a NullHandler

Another way to disable logging from an imported module is to create a NullHandler for the module's logger. A NullHandler is a logging handler that does nothing. It simply discards all messages sent to it. 

Here's an example of how to create a NullHandler and attach it to an imported module's logger:

```python
import logging
logging.getLogger("imported_module").addHandler(logging.NullHandler())
```

In this example, a NullHandler is created using the `logging.NullHandler()` method, and then attached to the "imported_module" logger using the `addHandler()` method. This will effectively disable all logging messages from the imported module without affecting any other logs in the application. 


## 3. Disable logging by blocking the module's loggers

A third way to disable logging from an imported module is to block all of its loggers by adding a `"propagate": False` key-value pair to the logger configuration dictionary.

Here's an example of how to block all loggers from the "imported_module":

```python
import logging
logging.getLogger("imported_module").handlers[0].propagate = False
```

In this example, the `"propagate": False` setting is added to the logger configuration for "imported_module". This will prevent any logs from being propagated up the logger hierarchy and effectively disable logging from the module.

# Conclusion

Disabling logging from imported modules is an important task for developers who want to reduce the noise level of their application's logging messages. By using one of the three methods outlined in this article, you can easily disable logging from any imported module within your application.
