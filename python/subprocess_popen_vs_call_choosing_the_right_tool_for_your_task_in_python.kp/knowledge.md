---
title: How can I utilize subprocess popen and call, and what sets them apart?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: subprocess Popen allows you to execute a command and interact with its inputs and outputs, while subprocess call only executes the command and returns its exit code.
---

**Contents**

[TOC]

## Introduction
When working with external commands or applications in Python, the subprocess module is a convenient way to launch and interact with them. Two commonly used functions in the subprocess module include `Popen()` and `call()`.

## The call() Function
The `call()` function is a simple way to execute a command and wait for it to complete. It takes a command as a list of arguments as its first argument and optionally accepts other arguments such as the current working directory, environment, and whether to capture and return the output.

Here's an example of using `call()` to execute the `ls` command on a Unix-based system:

```python
import subprocess

subprocess.call(['ls', '-l'])
```

In this example, we pass a list of arguments to the `call()` function. The first argument is the `ls` command, and the second is the `-l` flag. 

## The Popen() Function
The `Popen()` function is a more powerful way to interact with external commands as it provides more control over the process. Like `call()`, it also takes a command as a list of arguments and other optional arguments such as the current working directory, environment, and whether to capture and return the output. Additionally, `Popen()` allows you to control the process by sending input, capturing output, and setting timeouts.

Here's an example of using `Popen()` to execute the `ls` command and capture the output:

```python
import subprocess

result = subprocess.Popen(['ls', '-l'], stdout=subprocess.PIPE)
output = result.stdout.read()
print(output)
```

In this example, we use the `stdout=subprocess.PIPE` argument to capture the output of the `ls` command. We then read the output and store it in the `output` variable.

## Differences and Usage
The main difference between `call()` and `Popen()` is that `call()` is a simpler way to execute a command and wait for it to complete, while `Popen()` is a more powerful way to interact with the process.

If you simply want to execute a command and wait for it to complete, `call()` is the way to go. If you need more control over the process, such as capturing output or setting timeouts, `Popen()` is the better choice.

In general, if your goal is to simply execute a command and wait for it to finish, use `call()`. If you need more control over the process (such as capturing output, setting timeouts, etc.), use `Popen()`.
