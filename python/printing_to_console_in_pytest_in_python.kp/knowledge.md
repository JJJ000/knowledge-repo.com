---
title: What is the syntax for printing to the console using pytest?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can print to the console in pytest by using the `print()` function.
---

**Contents**

[TOC]

# Section 1: Importing the Logging Module

The first step to printing to the console in pytest is to import the logging module. This can be done with the following code:

```py
import logging
```

# Section 2: Setting the Logger

The next step is to set the logger. This can be done with the following code:

```py
logger = logging.getLogger()
logger.setLevel(logging.INFO)
```

# Section 3: Setting the Logging Handler

The third step is to set the logging handler. This can be done with the following code:

```py
handler = logging.StreamHandler()
handler.setLevel(logging.INFO)
logger.addHandler(handler)
```

# Section 4: Logging the Output

The final step is to log the output. This can be done with the following code:

```py
logger.info('This is the output that will be printed to the console')
```
