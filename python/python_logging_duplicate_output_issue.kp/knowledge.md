---
title: When making use of the Python logging module, there is an occurrence of repeat log output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: This can happen if multiple handlers are added to the logger.
---

**Contents**

[TOC]

1. Introduction

The Python logging module is a powerful tool that allows developers to control the level and format of log output. However, a common issue that developers run into is duplicate log output, where the same log message is printed multiple times. In this article, we will discuss some of the causes of duplicate log output and how to address them.

2. Root Cause Analysis

The root cause of duplicate log output is often due to misconfigured loggers or handlers. When a logger is misconfigured, it can create multiple instances of the logger that are registered with the logging module. Similarly, a handler can also create multiple instances of itself if it is not properly configured. As a result, when a log message is emitted, it can be processed by multiple handlers or loggers, leading to duplicate output.

3. Solution Strategy

To address duplicate log output, we need to ensure that our loggers and handlers are properly configured and registered with the logging module. This can involve checking the configuration of existing loggers and handlers, as well as ensuring that only one instance of each logger and handler is created. In cases where multiple loggers or handlers are required, we can use filters to ensure that log messages are only processed by the desired handlers.

4. Implementation Steps

The following steps can be taken to address duplicate log output in Python:

- Review the log configuration and ensure that all loggers and handlers are properly configured and registered with the logging module
- Check for multiple instances of loggers or handlers and eliminate any duplicates
- Use filters to ensure that log messages are only processed by the desired handlers
- Use the `propagate` attribute of loggers to control whether log messages are passed on to parent loggers, which can also result in duplicate output if misconfigured

By taking these steps, we can ensure that log messages are processed only once and eliminate duplicate log output.
