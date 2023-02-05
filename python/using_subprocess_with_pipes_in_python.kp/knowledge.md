---
title: What is the syntax for using the "subprocess" command with pipes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The subprocess module can be used to create pipelines by passing one process`s stdout as another process`s stdin.
---

**Contents**

[TOC]

##### Overview
The `subprocess` module in Python allows users to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. This can be useful for running shell commands and piping the output to another command.

##### Setting Up
The `subprocess` module provides several functions, including `Popen()` which takes a list of command-line arguments and returns an object representing the new process. The `stdin`, `stdout`, and `stderr` arguments can be used to specify the pipes to be used for input/output/error.

##### Running a Command
Once the `Popen()` object is created, the `communicate()` method can be used to run the command and get the output. The `communicate()` method takes an optional argument, `input`, which can be used to pass data to the command's standard input pipe.

##### Example
Here is an example of using the `subprocess` module to run a command with a pipe:

```python
import subprocess

# Create the Popen object
p = subprocess.Popen(['ls', '-l'], stdout=subprocess.PIPE)

# Run the command and get the output
output, _ = p.communicate()

# Print the output
print(output.decode())
```

This example runs the `ls -l` command and prints the output to the console.
