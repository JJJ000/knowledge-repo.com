---
title: What is the process of creating a daemon using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To create a daemon in Python, you need to detach a process from the parent process and run it in the background using the os module.
---

**Contents**

[TOC]

Introduction

A daemon is a long-running background process that performs some service for the system. In Python, creating a daemon involves a few steps that ensure the process runs as a daemon, creates a PID file, and redirects standard I/O streams.

Section 1: Fork the Process

The first step in creating a daemon is to fork the process. This creates a child process that is independent of the parent process. To do this, use the `os.fork()` method, which returns the ID of the child process in the parent process and 0 in the child process.

```python
import os

pid = os.fork()

if pid > 0:
    # exit parent process
    sys.exit(0)
```

In the above code, the parent process exits if the child process was created successfully.

Section 2: Change the Working Directory

The next step is to change the working directory to prevent the daemon from occupying the same directory as the parent process. This is important because the parent and the child could conflict if they try to access the same files or directories.

```python
os.chdir('/')
```

In the above code, the working directory is changed to the root directory.

Section 3: Redirect Standard Input, Output, and Error Streams

The next step is to redirect standard input, output, and error streams to a log file. This is necessary to free up the terminal and ensure the daemon runs in the background.

```python
sys.stdin.close()
sys.stdout = open('/var/log/daemon.log', 'a')
sys.stderr = open('/var/log/daemon.log', 'a')
```

The above code closes standard input and redirects standard output and error streams to a log file.

Section 4: Create a PID File

The final step is to create a PID file indicating the process ID of the daemon. This file is used to check if the daemon is already running.

```python
pid_file = '/var/run/daemon.pid'

if os.path.exists(pid_file):
    print('Daemon already running with PID:{}'.format(pid))
    sys.exit(0)

with open(pid_file, 'w') as f:
    f.write(str(os.getpid()))
``` 

In the above code, the PID file is created if it doesn't exist. The process ID of the daemon is written to the file, and the script exits.

Conclusion

Creating a daemon in Python involves forking the process, changing the working directory, redirecting standard I/O streams, and creating a PID file. These steps ensure the daemon runs as a background process and can be easily managed by the system.
