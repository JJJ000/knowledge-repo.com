---
title: What is the process for creating environment variables in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Environment variables in Python can be set using the os.environ dictionary.
---

**Contents**

[TOC]

## Using os.environ

The `os.environ` module can be used to set environment variables in Python. It provides access to the underlying operating system's environment variables. To set an environment variable, use the `os.environ` dictionary:

```python
import os
os.environ['MY_VAR'] = 'my_value'
```

## Using os.putenv

Another way to set environment variables in Python is to use the `os.putenv` function. This function takes two arguments: the environment variable name and its value:

```python
import os
os.putenv('MY_VAR', 'my_value')
```

## Using subprocess

The `subprocess` module provides a way to set environment variables in Python. The `subprocess.Popen` function can be used to set environment variables by passing a dictionary of environment variables as the `env` argument:

```python
import subprocess
env = {'MY_VAR': 'my_value'}
subprocess.Popen(['my_command'], env=env)
```

## Using dotenv

The `dotenv` library can be used to set environment variables in Python. This library allows you to define environment variables in a `.env` file and then load them into your application. To set an environment variable with `dotenv`, create a `.env` file in the root of your project and add the environment variable to it:

```
MY_VAR=my_value
```

Then, use the `dotenv.load_dotenv` function to load the environment variables from the `.env` file:

```python
import dotenv
dotenv.load_dotenv()
```
