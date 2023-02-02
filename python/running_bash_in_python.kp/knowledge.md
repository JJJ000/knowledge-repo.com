---
title: Executing bash commands from within a Python script
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Python can run Bash commands using the subprocess module.
---

**Contents**

[TOC]

## Using the Subprocess Module
The [subprocess](https://docs.python.org/3/library/subprocess.html) module allows you to run Bash commands in Python. This is done by creating a subprocess object and then calling the `run()` method on it.

## Example
The following example shows how to use the `subprocess` module to run the Bash command `ls -l`:

```python
import subprocess

subprocess.run(['ls', '-l'])
```

## Capturing Output
The `run()` method also allows you to capture the output of the command by setting the `stdout` parameter to `subprocess.PIPE`:

```python
import subprocess

output = subprocess.run(['ls', '-l'], stdout=subprocess.PIPE).stdout
```

## Error Handling
The `run()` method also allows you to check for errors by setting the `stderr` parameter to `subprocess.PIPE` and then checking the `returncode` attribute of the subprocess object:

```python
import subprocess

try:
    output = subprocess.run(['ls', '-l'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)
except subprocess.CalledProcessError as e:
    print('Command failed:', e.returncode)
```
