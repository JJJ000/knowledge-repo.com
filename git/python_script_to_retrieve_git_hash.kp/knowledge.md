---
title: Retrieve the most recent git commit hash within a Python program
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the subprocess module to run the `git rev-parse HEAD` command and store the output in a variable.
---

**Contents**

[TOC]

# Using the subprocess Module

Python's `subprocess` module can be used to get the current git hash from within a Python script. The following code snippet shows an example of how to do this:

```python
import subprocess

# Get the current git hash
git_hash = subprocess.check_output(["git", "rev-parse", "HEAD"]).decode("utf-8").strip()

print(git_hash)
```

# Using the gitpython Module

The `gitpython` module can also be used to get the current git hash from within a Python script. The following code snippet shows an example of how to do this:

```python
import git

# Get the current git hash
repo = git.Repo(search_parent_directories=True)
git_hash = repo.head.object.hexsha

print(git_hash)
```

# Using the Git Command Line

The git command line can also be used to get the current git hash from within a Python script. The following code snippet shows an example of how to do this:

```python
import os

# Get the current git hash
git_hash = os.popen("git rev-parse HEAD").read().strip()

print(git_hash)
```
