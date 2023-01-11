---
title: What is the process of retrieving environment variables in Python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can access environment variables in Python using the os.environ dictionary.
---

**Contents**

[TOC]

### Using os.environ

The most common way to access environment variables in Python is by using the `os.environ` object. This object contains a mapping of all the environment variables that are currently set. To access a specific environment variable, you can use the `os.environ` object's `get` method, passing in the name of the environment variable as a string.

For example, to access the `PATH` environment variable, you can do the following:

```python
import os

path = os.environ.get('PATH')
```

### Using os.getenv

Alternatively, you can use the `os.getenv` method to access environment variables. This method is essentially a shorthand for the `os.environ.get` method, and it takes the same arguments.

For example, to access the `PATH` environment variable, you can do the following:

```python
import os

path = os.getenv('PATH')
```

### Using os.putenv

The `os.putenv` method can be used to set environment variables. This method takes two arguments: the name of the environment variable and the value to set it to.

For example, to set the `PATH` environment variable, you can do the following:

```python
import os

os.putenv('PATH', '/usr/bin')
```

### Using subprocess.Popen

The `subprocess.Popen` method can be used to run a command in a subprocess and access its environment variables. This method takes a `env` argument, which is a mapping of environment variables to set for the subprocess.

For example, to run a command with the `PATH` environment variable set to `/usr/bin`, you can do the following:

```python
import subprocess

subprocess.Popen(['ls', '-l'], env={'PATH': '/usr/bin'})
```
