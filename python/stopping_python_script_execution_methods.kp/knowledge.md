---
title: What is the process to stop the running of a Python script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Press Ctrl+C.
---

**Contents**

[TOC]

# Using keyboard interrupt

The simplest way to abort the execution of a Python script is to use a keyboard interrupt. This can be done by pressing the `Ctrl + C` combination on the keyboard. This will immediately stop the execution of the program, but it may not be the most graceful way to terminate a script.

```python
try:
    # Your code
except KeyboardInterrupt:
    print('Execution aborted.')
```

# Using SystemExit

Another way is to raise a SystemExit exception. This will immediately stop the execution of the script and raise an exception. It's a slightly more elegant way to terminate a script, and you can catch the exception to perform cleanup operations before exiting.

```python
import sys

try:
    # Your code
except SystemExit:
    sys.exit('Execution aborted.')
```

# Using signals

On Unix-based systems, you can also use signals to gracefully terminate a script. The most common signal used for this purpose is the SIGTERM signal. This signal can be caught using the `signal` library and used to perform cleanup operations before exiting.

```python
import signal

def signal_handler(signum, frame):
    # Your cleanup code
    print('Execution aborted.')
    sys.exit(0)

signal.signal(signal.SIGTERM, signal_handler)

# Your code
```

# Using threading

Finally, you can use threads to run your main code in a separate thread, and the main thread can be used to listen for a signal to gracefully exit. This approach is useful if your code is long-running and you want to be able to terminate it from another thread or process.

```python
import threading

class MyThread(threading.Thread):
    def __init__(self):
        super(MyThread, self).__init__()

    def run(self):
        # Your long-running code

t = MyThread()
t.start()

signal.signal(signal.SIGTERM, lambda signum, frame: t.join())

# Your listener code in the main thread
```
