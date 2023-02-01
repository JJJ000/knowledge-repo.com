---
title: What is the best way to handle sigint in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can capture SIGINT in Python by using the signal module`s signal.signal() function.
---

**Contents**

[TOC]

# Using the Signal Module
The Python Standard Library provides a signal module which can be used to capture and respond to SIGINT signals. The signal module provides a signal() function which takes two arguments: the signal number and a function to be called when the signal is received. 

To capture a SIGINT signal, the signal() function should be called with signal number 2 (SIGINT) and a function to be called when the signal is received. The following example shows how to capture and respond to a SIGINT signal:

```python
import signal

def handle_sigint(signum, frame):
    print('SIGINT received!')

signal.signal(signal.SIGINT, handle_sigint)
```

# Using the KeyboardInterrupt Exception
A KeyboardInterrupt exception can be used to capture and respond to SIGINT signals. This exception is raised when a SIGINT signal is received by the Python interpreter. The following example shows how to capture and respond to a SIGINT signal:

```python
try:
    while True:
        # Do something
        pass
except KeyboardInterrupt:
    print('SIGINT received!')
```
