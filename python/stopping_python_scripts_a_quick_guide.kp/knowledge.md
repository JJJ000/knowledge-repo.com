---
title: What is the process for ending/discontinuing the execution of a Python script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Press Ctrl+C in the terminal/command prompt where the script is running to stop it.
---

**Contents**

[TOC]

## Option 1: Use Ctrl+C

The easiest way to stop a running Python script is to use the `Ctrl+C` keyboard shortcut. This sends an interrupt signal to the running process and the program will terminate after performing any necessary clean-up tasks.

However, if the script is running in a background process or on a remote server, this method may not work.

## Option 2: Use os.kill()

The `os` module provides a way to terminate a running process using its PID (process identifier). First, you need to find the PID of the process using system tools or `psutil` module. 

Then, you can use the `os.kill()` function to send a termination signal to the specified process.

```python
import os

pid = 1234  # replace with the PID of the running process
os.kill(pid, signal.SIGTERM)  # send termination signal
```

## Option 3: Use sys.exit()

If you have control over the running script, you can use the `sys.exit()` function to terminate the program from within the script.

```python
import sys

# some code...
sys.exit()  # terminate program
```

You can also pass a status code to `sys.exit()` to indicate the reason for termination.

```python
import sys

# some code...
sys.exit(1)  # terminate program with exit code 1
```

## Option 4: Use threading.Event()

If your Python script is running in a separate thread, you can use a `threading.Event()` object to signal the thread to stop running.

```python
import threading

stop_event = threading.Event()

# in your thread function...
while not stop_event.is_set():
  # some code...
  
# to stop the thread...
stop_event.set()
```

When the `stop_event` is set, the running thread will exit gracefully.
