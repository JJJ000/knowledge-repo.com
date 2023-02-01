---
title: Configuring Python loggers to write all messages to both the log file and standard output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To have Python loggers output all messages to stdout in addition to the log file, set the logger`s stream handler to stdout.
---

**Contents**

[TOC]

1. Overview
--------------------------------
Python logging module provides a way to use logging in applications. Logging can be used to track errors, debug issues, and provide useful information. It is also possible to configure loggers to output messages to both a log file and to standard output (stdout). This article will discuss how to configure loggers to output all messages to both stdout and log files.

2. Configure Loggers
--------------------------------
To configure loggers to output all messages to both stdout and log files, first create a logger object and set the logging level to the desired level (e.g. DEBUG). Then, create a StreamHandler object and set the stream to sys.stdout. Finally, add the StreamHandler object to the logger object.

```
import logging
import sys

logger = logging.getLogger('my_logger')
logger.setLevel(logging.DEBUG)

handler = logging.StreamHandler(sys.stdout)
logger.addHandler(handler)
```

3. Create Log File Handler
--------------------------------
To also output messages to a log file, create a FileHandler object and set the filename to the desired log file. Then, add the FileHandler object to the logger object.

```
handler = logging.FileHandler('my_log_file.log')
logger.addHandler(handler)
```

4. Logging Messages
--------------------------------
Once the logger is configured, messages can be logged using the logger object.

```
logger.debug('This is a debug message')
logger.info('This is an info message')
logger.warning('This is a warning message')
logger.error('This is an error message')
logger.critical('This is a critical message')
```

The messages will be output to both stdout and the log file.
