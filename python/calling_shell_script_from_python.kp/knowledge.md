---
title: What is the method for executing a shell script through Python code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can call a shell script from Python code using the `subprocess` module.
---

**Contents**

[TOC]

## Section 1: Introduction

In many cases, we may want to execute a shell script from our Python code. This can be done using a few methods. In this tutorial, we will discuss how to call a shell script from Python, and we will explore different ways to achieve this.

## Section 2: Using the subprocess module

The `subprocess` module is included in Python's standard library, and it allows us to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. We can use this module to execute a shell script from our Python code.

Here is an example of how to use `subprocess` to call a shell script:

```python
import subprocess

subprocess.call(['./my_script.sh'])
```

This will run the `my_script.sh` shell script located in the current working directory.

We can also pass arguments to the shell script by adding them to the list:

```python
subprocess.call(['./my_script.sh', 'arg1', 'arg2'])
```

## Section 3: Using the os module

The `os` module provides a way to interact with the operating system in Python. We can use this module to execute a shell script from our Python code. Here is an example:

```python
import os

os.system('./my_script.sh')
```

This will run the `my_script.sh` shell script located in the current working directory. We can also pass arguments to the shell script by including them in the command:

```python
os.system('./my_script.sh arg1 arg2')
```

## Section 4: Using the subprocess.run() function

The `subprocess.run()` function was added in Python 3.5. This function provides a simpler and more powerful interface for spawning new processes and retrieving their output. Here is an example of how to use it to call a shell script:

```python
import subprocess

subprocess.run(['./my_script.sh'], check=True)
```

This will run the `my_script.sh` shell script located in the current working directory, and it will raise an error if the shell script returns a non-zero exit code. We can also pass arguments to the shell script by including them in the list:

```python
subprocess.run(['./my_script.sh', 'arg1', 'arg2'], check=True)
```

## Conclusion

In this tutorial, we discussed how to execute a shell script from Python code. We explored three different ways to achieve this: using the subprocess module, using the os module, and using the subprocess.run() function. Each of these methods has its advantages and disadvantages, so it's up to the developer to choose the one that best fits their needs.
