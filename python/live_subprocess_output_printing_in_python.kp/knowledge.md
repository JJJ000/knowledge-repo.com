---
title: Print the output of the subprocess continuously as long as the process is running
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `subprocess.Popen` constructor with the `stdout` argument set to `subprocess.PIPE`, and call `communicate()` or `stdout.read()` in a loop to continuously read and display the output until the process is complete.
---

**Contents**

[TOC]

## Using Popen with PIPE

The first method to constantly print subprocess output while a process is running is to use `Popen` with `PIPE`. 
 
```
from subprocess import Popen, PIPE

process = Popen(command, stdout=PIPE, stderr=PIPE)

while True:
    output = process.stdout.readline()
    if output == '' and process.poll() is not None:
        break
    if output:
        print(output.strip())
```
  
In this code snippet, the `command` variable is a list of strings that represent the command and its arguments. 
 
The `Popen` function starts the process and captures its standard output and error pipes. 
 
The while loop reads the standard output pipe of the process, line by line, and prints them as they are available. 
 
Finally, if the process has finished, the loop ends.


## Using communicate

Another method to constantly print subprocess output while a process is running is to use the `communicate` method. 

```
from subprocess import Popen, PIPE

process = Popen(command, stdout=PIPE, stderr=PIPE)

while True:
    output, error = process.communicate()
    if not output and not error:
        break
    print(output, end='')
```

In this code snippet, the `command` variable is a list of strings that represent the command and its arguments.

The `Popen` function starts the process and captures its standard output and error pipes.

The `communicate` method reads the output and error pipes of the process, waits for the process to finish, and returns them as a tuple.

Finally, the loop ends when there is no more output or error to read.

## Using select

A third method to constantly print subprocess output while a process is running is to use the `select` module.

```
import os
import select
from subprocess import Popen, PIPE

process = Popen(command, stdout=PIPE, stderr=PIPE)

while True:
    # Use select to wait for pipe availability and avoid blocking
    read_fds, _, _ = select.select([process.stdout, process.stderr], [], [])
    for pipe in read_fds:
        if pipe == process.stdout:
            output = os.read(pipe.fileno(), 1024)
            if not output:
                break
            print(output.decode(), end='')
        elif pipe == process.stderr:
            error = os.read(pipe.fileno(), 1024)
            if not error:
                break
            print(error.decode(), end='')
    if process.poll() is not None:
        break
```

In this code snippet, the `command` variable is a list of strings that represent the command and its arguments.

The `Popen` function starts the process and captures its standard output and error pipes.

The `select` function is called to wait for an available pipe to read. By doing so, we avoid blocking the loop when the pipes are empty.

The `os.read` function is called to read the available output or error up to 1024 bytes.

Finally, the loop ends when the process has finished.
