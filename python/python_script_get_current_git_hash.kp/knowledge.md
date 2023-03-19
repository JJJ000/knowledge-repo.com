---
title: Obtain the present git hash in a Python code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To get the current git hash in a Python script, use the command `git rev-parse HEAD` and capture the output using subprocess module.
---

**Contents**

[TOC]

## Using GitPython library

We can use the GitPython library to get the current git hash in a Python script. This library is a pythonic interface for Git that allows us to interact with Git repositories in Python.

```python
import git

repo = git.Repo(search_parent_directories=True)
current_hash = repo.head.object.hexsha
print(current_hash)
```

The `search_parent_directories` argument tells GitPython to search for the git repository in the parent directories if it's not found in the current directory.


## Using subprocess module

We can also use the `subprocess` module to execute a git command and capture its output. Since we only need the git hash, we can use the `git rev-parse HEAD` command to get it.

```python
import subprocess

current_hash = subprocess.check_output(['git', 'rev-parse', 'HEAD']).strip().decode('utf-8')
print(current_hash)
```

The `check_output` function runs the command specified as a list of strings and returns its output. We use the `strip` method to remove any trailing whitespace and the `decode` method to convert the output from bytes to a string.


## Using os module

We can also use the `os` module to execute a git command and capture its output, similar to the `subprocess` module solution.

```python
import os

current_hash = os.popen('git rev-parse HEAD').read().strip()
print(current_hash)
```

The `os.popen` function runs the command specified as a string and returns a file object, which we can read using the `read` method. Finally, we use the `strip` method to remove any trailing whitespace.
