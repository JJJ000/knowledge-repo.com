---
title: Can you tell me the location of the pip cache directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The pip cache folder in Python is located at `~/.cache/pip` on Unix-based systems or `%HOME%\AppData\Local\pip\Cache` on Windows.
---

**Contents**

[TOC]

### Introduction
When working with Python packages you often use pip to install and manage them. Pip stores downloaded packages in a cache for future use. This cache folder can be useful for debugging or troubleshooting issues with package installations. In this article, we will discuss where the pip cache folder is located in Python.

### Finding the pip cache folder
The location of the pip cache folder depends on your operating system. Here are the locations of the pip cache folder for some common operating systems:

#### Windows
On Windows, the pip cache folder is located at:
```
%USERPROFILE%\AppData\Local\pip\Cache
```

#### macOS and Linux
On macOS and Linux, the pip cache folder is located at:
```
~/.cache/pip
```

#### Custom location
You can set a custom location for the pip cache folder by setting the `PIP_CACHE_DIR` environment variable. For example, to set the pip cache folder to `/custom/path/pip-cache`, run the following command:
```
export PIP_CACHE_DIR=/custom/path/pip-cache
```

### Conclusion
The pip cache folder is useful for troubleshooting, debugging, and speeding up package installations. In this article, we discussed where the pip cache folder is located on different operating systems and how to set a custom location. We hope you found this article helpful.
