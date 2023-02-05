---
title: Implementing logging across multiple modules
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Logging can be used in multiple modules in Python by creating a logger object in each module and setting the logging level appropriately.
---

**Contents**

[TOC]

## Setup

To use logging in multiple modules, you will need to set up the logging module in each module. This can be done by importing the logging module and then calling the `basicConfig()` function, which sets up the logging configuration.

## Logging Configuration

The `basicConfig()` function takes a variety of parameters, such as the log level, log file name, and format of the log messages. It is important to use the same configuration in each module to ensure consistency in the log messages.

## Logging Messages

Once the logging module is set up, you can begin logging messages. This is done by calling the `logging.info()`, `logging.warning()`, or `logging.error()` functions, depending on the severity of the message. These functions take a string message as a parameter.

## Logging Output

The logging messages will be output to the log file that was specified in the `basicConfig()` function. This file can then be used to review the logged messages.
