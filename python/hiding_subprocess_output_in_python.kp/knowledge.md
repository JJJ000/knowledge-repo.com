---
title: What is the best way to conceal the output of a subprocess?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the subprocess.run() function with the `stdout=subprocess.DEVNULL` argument.
---

**Contents**

[TOC]

# 1. Using the subprocess.DEVNULL

The simplest way to hide the output of a subprocess in Python is to use the subprocess.DEVNULL argument. This argument is a special file-like object that can be used as the destination for subprocess output. By using this argument, any output from the subprocess will be discarded.

Example:

```
import subprocess

subprocess.run(["echo", "Hello World!"], stdout=subprocess.DEVNULL)
```

# 2. Redirecting Output Streams

Another way to hide the output of a subprocess in Python is to redirect the output streams. This can be done by setting the stdout and stderr arguments of the subprocess.run() function to a file-like object. By redirecting the output streams, any output from the subprocess will be written to the file-like object instead of the terminal.

Example:

```
import subprocess

with open("output.txt", "w") as f:
    subprocess.run(["echo", "Hello World!"], stdout=f, stderr=f)
```

# 3. Capturing Output in a Variable

Another way to hide the output of a subprocess in Python is to capture the output in a variable. This can be done by setting the stdout and stderr arguments of the subprocess.run() function to subprocess.PIPE. This will capture any output from the subprocess in a variable that can then be used for further processing.

Example:

```
import subprocess

output = subprocess.run(["echo", "Hello World!"], stdout=subprocess.PIPE, stderr=subprocess.PIPE).stdout
```

# 4. Suppressing Output with the Popen Constructor

Finally, the output of a subprocess can be hidden by using the Popen constructor instead of the run() function. The Popen constructor allows for more control over how the subprocess is run, including the ability to suppress output. This can be done by setting the stdout and stderr arguments to subprocess.DEVNULL.

Example:

```
import subprocess

p = subprocess.Popen(["echo", "Hello World!"], stdout=subprocess.DEVNULL, stderr=subprocess.DEVNULL)
p.wait()
```
