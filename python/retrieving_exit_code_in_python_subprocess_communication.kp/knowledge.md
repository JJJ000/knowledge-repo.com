---
title: What is the method to obtain the exit code while utilizing the Python subprocess communicate function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the returncode attribute of the CompletedProcess object returned by the communicate method.
---

**Contents**

[TOC]

## Introduction
Python's subprocess module is used to create new processes and interacts with the input and output streams of the process. There are several methods available in the subprocess module to interact with child processes. One of those methods is `communicate`, which allows you to communicate with the process and get its return code.

## Using subprocess communicate method
The `communicate` method is used to interact with the process and it waits for the process to complete before returning. Here's an example of how to use it:

``` python
import subprocess

process = subprocess.Popen(['ls', '-al'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

stdout, stderr = process.communicate()

print("stdout:", stdout)
print("stderr:", stderr)
```

In the above example, we are running the `ls -al` command and capturing its output using the `communicate` method.

## Getting the exit code
When the process completes, it returns an exit code. The exit code represents the status of the process. If the process completes successfully, it returns 0. If it fails, it returns a non-zero value, which indicates the reason for failure.

To get the exit code, you can use the `returncode` attribute of the `Popen` object. Here's how to modify the previous example to get the exit code:

``` python
import subprocess

process = subprocess.Popen(['ls', '-al'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

stdout, stderr = process.communicate()

print("Exit code:", process.returncode)
```

In the above example, we are using the `returncode` attribute to get the exit code of the process.

## Handling error conditions
When you encounter an error while running a process, the `returncode` value will be non-zero. You can catch these errors by checking the value of `returncode` and taking appropriate action.

``` python
import subprocess

process = subprocess.Popen(['ls', 'nonexistent_file'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

stdout, stderr = process.communicate()

if process.returncode != 0:
    print("Error:", stderr.decode())
```

In the above example, we are running the `ls nonexistent_file` command, which will result in an error. We are checking the `returncode` attribute and printing the error message if it's non-zero.

## Conclusion
The `communicate` method is an easy way to interact with a child process and get its exit code. You can use the `returncode` attribute of the `Popen` object to get the exit code, and handle error conditions by checking the value of `returncode`.
