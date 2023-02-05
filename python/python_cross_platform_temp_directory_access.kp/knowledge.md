---
title: Finding the temporary directory in Python across different platforms
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The tempfile module provides a cross-platform way of getting the system`s temporary directory in Python.
---

**Contents**

[TOC]

### os.environ

The `os.environ` module provides an easy way to get the temporary directory on any platform. The `os.environ` module contains a list of environment variables, including the `TEMP` variable, which returns the path of the system's temporary directory.

### tempfile

The `tempfile` module provides a more robust way to get the temporary directory on any platform. The `tempfile.gettempdir()` function returns the path of the system's temporary directory.

### tempdir

The `tempdir` module provides an easy way to create a temporary directory on any platform. The `tempdir.TemporaryDirectory()` function creates a temporary directory and returns its path.

### shutil

The `shutil` module provides an easy way to create a temporary directory on any platform. The `shutil.mkdtemp()` function creates a temporary directory and returns its path.
