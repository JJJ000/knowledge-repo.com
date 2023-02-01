---
title: Performing a non-blocking read from a subprocess.pipe in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: A non-blocking read on a subprocess.PIPE in Python can be achieved using the select module.
---

**Contents**

[TOC]

#Section 1: Overview

A non-blocking read on a subprocess.PIPE in Python is a way to read from a subprocess without blocking the main program. This means that the main program can continue executing while the subprocess is running in the background. The non-blocking read allows the main program to check for new data from the subprocess without waiting for it to finish.

#Section 2: How it Works

The non-blocking read is accomplished by using the select() function in the select module. This function monitors multiple file descriptors and returns when any of them is ready for reading. The select() function takes a list of file descriptors, including the subprocess.PIPE, and a timeout value. The timeout value determines how long the select() function will wait for data to be available before returning.

#Section 3: Example

The following example shows how to use the select() function to perform a non-blocking read on a subprocess.PIPE.

```
import select

# Create a subprocess
proc = subprocess.Popen(['cat', 'myfile.txt'], stdout=subprocess.PIPE)

# Create a list of file descriptors to monitor
fds = [proc.stdout]

# Set a timeout value
timeout = 10

# Monitor the file descriptors
ready = select.select(fds, [], [], timeout)

# Check if any of the file descriptors are ready for reading
if ready[0]:
    # Read from the subprocess
    data = proc.stdout.read()
```

#Section 4: Conclusion

Non-blocking reads on a subprocess.PIPE in Python are an efficient way to read from a subprocess without blocking the main program. The select() function is used to monitor multiple file descriptors and return when any of them is ready for reading. The example above shows how to use the select() function to perform a non-blocking read on a subprocess.PIPE.
