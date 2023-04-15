---
title: If the directories don't exist, python's pathlib creates them
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To create a directory path in Python pathlib, you can use the .mkdir(parents=True, exist\_ok=True) method, which creates all parent directories (if they don’t exist) and creates the directory (if it doesn’t exist).
---

**Contents**

[TOC]

1. Introduction
Python's pathlib module provides an intuitive way to work with file paths in a platform-independent way. One of the common requirements while working with file paths is to create directories if they don't exist. In this article, we will explore various ways to create directories using the pathlib module.

2. Creating directories using pathlib.Path.mkdir()
The simplest way to create a directory using pathlib is by using the mkdir() method. The mkdir() method creates a directory at the specified path if it doesn't already exist. Here's an example:

```python
from pathlib import Path

path = Path('/path/to/my/directory')
path.mkdir(parents=True, exist_ok=True)
```

In the above example, we create a Path object with the directory path and call the mkdir() method on it. The parents=True parameter ensures that any intermediate directories are also created if they don't already exist. The exist_ok=True parameter ensures that no errors are raised if the directory already exists.

3. Creating directories using pathlib.Path.resolve()
Another way to create a directory using pathlib is by using the resolve() method. The resolve() method returns the absolute path of the given path, and creates the directories in the path if they don't exist. Here's an example:

```python
from pathlib import Path

path = Path('/path/to/my/directory')
abs_path = path.resolve()
```

In the above example, we create a Path object with the directory path and call the resolve() method on it. The abs_path variable contains the absolute path of the directory, and the directories in the path are created if they don't already exist.

4. Conclusion
In this article, we explored various ways to create directories using the Python pathlib module. We discussed the mkdir() method and the resolve() method, and demonstrated how to create directories if they don't already exist. These methods make it straightforward to work with file paths in Python, and we encourage developers to explore the other features of the pathlib module.
