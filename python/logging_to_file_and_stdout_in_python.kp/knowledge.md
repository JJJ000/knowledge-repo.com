---
title: Configuring the logger to output log messages to both a file and the standard output stream
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Configure the logging module to use a StreamHandler to log to stdout, and a FileHandler to log to a file.
---

**Contents**

[TOC]

# Logging to File

Python supports logging to a file using the `logging` module. To configure the logger to log to a file, use the `basicConfig()` method to set the filename and other options.

```python
import logging

logging.basicConfig(filename='log.txt', level=logging.DEBUG)
```

# Logging to Stdout

Python supports logging to stdout using the `logging` module. To configure the logger to log to stdout, use the `basicConfig()` method to set the stream option to `sys.stdout`.

```python
import logging
import sys

logging.basicConfig(stream=sys.stdout, level=logging.DEBUG)
```

# Combining Logging to File and Stdout

Python supports logging to both a file and stdout using the `logging` module. To configure the logger to log to both, use the `basicConfig()` method to set the filename and stream option.

```python
import logging
import sys

logging.basicConfig(filename='log.txt', stream=sys.stdout, level=logging.DEBUG)
```

# Logging Format

Python supports customizing the format of log messages using the `logging` module. To configure the format of log messages, use the `basicConfig()` method to set the `format` option.

```python
import logging

logging.basicConfig(format='%(asctime)s - %(name)s - %(levelname)s - %(message)s', level=logging.DEBUG)
```
