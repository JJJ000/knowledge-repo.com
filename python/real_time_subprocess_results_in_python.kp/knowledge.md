---
title: The real-time or immediate response of a subprocess command
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use subprocess.Popen() to open and run the command, then use communicate() to obtain the output as a string.
---

**Contents**

[TOC]

## Introduction 

`subprocess` is a powerful module in Python that provides us a way to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. One common task when working with the `subprocess` module is to capture the live output of a command. 

In this article, we will explore different methods to capture live output from subprocess command in Python.

## Method 1: Using communicate()

One way to capture live output from subprocess command is by using the `communicate()` method. This method reads all the output from the subprocess until it terminates.

Here is an example:

```python
import subprocess

process = subprocess.Popen(['ping', '-c', '5', 'google.com'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

while True:
    output = process.stdout.readline()
    if output == b'' and process.poll() is not None:
        break
    if output:
        print(output.strip())
```

In this example, we used the `PIPE` constant to redirect the process output to a pipe. Then, we used a loop to read the output line by line until the process terminates.

## Method 2: Using select()

Another way to capture live output from subprocess command is by using the `select` module. This module allows us to wait for some I/O operation to occur.

Here is an example:

```python
import subprocess
import select

process = subprocess.Popen(['ping', '-c', '5', 'google.com'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

while True:
    ready, _, _ = select.select([process.stdout, process.stderr], [], [], 1.0)
    if not ready:
        break
    for io in ready:
        print(io.readline().strip())
```

In this example, we used the `select` module to wait until there is some data to be read from the process output. Then, we used a loop to read the output line by line until there is no more data to read.

## Method 3: Using threading

A third way to capture live output from subprocess command is by using threading. This method spawns a new thread that continuously reads the process output.

Here is an example:

```python
import subprocess
import threading

def read_output(process):
    for c in iter(lambda: process.stdout.read(1), b''):
        print(c.decode(), end='')

process = subprocess.Popen(['ping', '-c', '5', 'google.com'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

thread = threading.Thread(target=read_output, args=(process,))
thread.start()

while thread.is_alive():
    thread.join(1)
```

In this example, we defined a new function `read_output` that reads the output character by character until there is no more data to read. Then, we spawned a new thread to run this function continuously. Finally, we waited for the thread to finish. 

## Conclusion

We have explored different methods to capture live output from subprocess command in Python. Depending on the specific use case, one method may be more suitable than another. It's important to choose the right method to avoid performance issues or synchronization problems.
