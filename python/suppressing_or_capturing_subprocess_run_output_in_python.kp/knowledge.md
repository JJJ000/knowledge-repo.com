---
title: What are the ways to capture or suppress the output of subprocess.run()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To suppress the output of subprocess.run() in Python, set the parameter stdout=subprocess.DEVNULL, and to capture the output, set the parameter capture\_output=True.
---

**Contents**

[TOC]

## Introduction

In some cases, when using the `subprocess.run()` method in Python, you may want to suppress the standard output (STDOUT) or standard error (STDERR) in order to improve the readability of your code. Alternatively, you may want to capture this output so that you can use it later in your script. In this article, we will discuss how to achieve both of these objectives.

## Suppressing output

If you want to suppress the output of your subprocess, you can set the `stdout` and/or `stderr` arguments to `subprocess.DEVNULL`. This will redirect any STDOUT or STDERR output to the null device, effectively discarding it. Here is an example:

``` python
import subprocess

subprocess.run(["ls", "-l"], stdout=subprocess.DEVNULL, stderr=subprocess.DEVNULL)
```

This will execute the command `ls -l`, but will not display any output on the console.

## Capturing output

If you want to capture the output of your subprocess, you can set the `stdout` and/or `stderr` arguments to `subprocess.PIPE`. This will launch the subprocess in a way that allows you to capture its STDOUT and/or STDERR output. Here's an example:

``` python
import subprocess

result = subprocess.run(["ls", "-l"], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

print(result.stdout)
```

This will execute the command `ls -l`, and store the result in the `result` variable. We can then print the STDOUT output by accessing the `stdout` attribute of the `result` object.

## Redirecting output

In some cases, you may want to redirect the output of your subprocess to a file, rather than displaying it on the console or capturing it in a variable. You can do this by specifying a file object as the value of the `stdout` and/or `stderr` arguments. Here's an example:

``` python
import subprocess

with open("output.txt", "w") as f:
    subprocess.run(["ls", "-l"], stdout=f, stderr=f)
```

This will execute the command `ls -l`, and redirect both the STDOUT and STDERR output to a file called `output.txt`.

## Conclusion

In this article, we have discussed how to suppress, capture, and redirect the output of subprocesses in Python using the `subprocess.run()` method. By using these techniques, you can control how your subprocesses behave and integrate them more effectively into your Python scripts.
