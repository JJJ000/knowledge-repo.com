---
title: The issue of Python logging duplicating log messages
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This issue may occur if multiple handlers are added to the logger or if the logger is instantiated multiple times.
---

**Contents**

[TOC]

# Problem Description

When using Python's logging module, it is possible for log messages to appear twice in the output, even when there is only one logging call. This can lead to confusion and make it harder to read and understand logs.

# Possible Causes

There are several possible causes for log messages appearing twice:

1. Multiple handlers: If the same log message is being handled by multiple handlers, it may appear twice in the output.

2. Duplicate loggers: If multiple logger objects are created with the same name, the log messages may be duplicated.

3. Multiple calls to basicConfig: If basicConfig is called multiple times, it can result in duplicate log messages.

# Solution

Depending on the specific cause of the issue, there are several possible solutions:

1. Remove duplicate handlers: Check the configuration of your logger and remove any duplicate handlers that may be causing the issue.

2. Use a single logger: Instead of creating multiple logger objects, use a single logger instance throughout the code.

3. Call basicConfig only once: Ensure that basicConfig is only called once, ideally at the beginning of the script.

# Conclusion

By identifying the possible causes and implementing the appropriate solutions, it is possible to avoid duplicate log messages and ensure that logs are easy to read and understand. Proper logging is an essential component of effective application monitoring and troubleshooting, and it is important to pay attention to the details to ensure that logs provide the necessary insights.
