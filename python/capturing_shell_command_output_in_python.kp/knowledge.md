---
title: Executing a shell command and storing the results
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can capture the output of a shell command in Python using the subprocess module`s check\_output() function.
---

**Contents**

[TOC]

### Using the `subprocess` Module

The `subprocess` module is the recommended way to run shell commands in Python. It provides a number of functions for interacting with the operating system, including the `run()` function which can be used to execute shell commands and capture their output. 

For example, the following code will execute the `ls` command and capture the output in the `output` variable:

```python
import subprocess

result = subprocess.run(['ls'], stdout=subprocess.PIPE)
output = result.stdout.decode('utf-8')
```

### Using the `os` Module

The `os` module also provides functions for interacting with the operating system, including the `os.popen()` function which can be used to execute shell commands and capture their output. 

For example, the following code will execute the `ls` command and capture the output in the `output` variable:

```python
import os

output = os.popen('ls').read()
```

### Using the `commands` Module

The `commands` module is an older, less-recommended way to run shell commands in Python. It provides a number of functions for interacting with the operating system, including the `commands.getoutput()` function which can be used to execute shell commands and capture their output. 

For example, the following code will execute the `ls` command and capture the output in the `output` variable:

```python
import commands

output = commands.getoutput('ls')
```
