---
title: What is the most effective way to retrieve the system hostname using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the socket.gethostname() function to get the system hostname in Python.
---

**Contents**

[TOC]

# Using socket Library

The [socket library](https://docs.python.org/3/library/socket.html) provides access to the underlying operating system socket interfaces. The `gethostname()` function of the socket library can be used to get the system hostname.

Example:

```python
import socket

hostname = socket.gethostname()
print(hostname)
```

# Using platform Library

The [platform library](https://docs.python.org/3/library/platform.html) provides access to the underlying operating system. The `node()` function of the platform library can be used to get the system hostname.

Example:

```python
import platform

hostname = platform.node()
print(hostname)
```

# Using os Library

The [os library](https://docs.python.org/3/library/os.html) provides access to the underlying operating system. The `uname()` function of the os library can be used to get the system hostname.

Example:

```python
import os

hostname = os.uname()[1]
print(hostname)
```
