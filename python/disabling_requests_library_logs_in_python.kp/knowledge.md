---
title: What is the process for turning off log messages from the requests library?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can disable log messages from the Requests library in Python by setting the log level to `WARNING`.
---

**Contents**

[TOC]

1. **Using Logging**

The Requests library uses Python's logging module to provide log messages. To disable log messages from the Requests library, you can use the logging module to set the logging level for the logging.getLogger("requests") logger to logging.CRITICAL.

2. **Example Code**

The following code example shows how to disable log messages from the Requests library:

```python
import logging
logging.getLogger("requests").setLevel(logging.CRITICAL)
```

3. **Using Environment Variables**

Alternatively, you can also disable log messages from the Requests library by setting the REQUESTS_LOG environment variable to 0.

4. **Example Code**

The following code example shows how to disable log messages from the Requests library using environment variables:

```bash
export REQUESTS_LOG=0
```
