---
title: The installation of packages was not possible because of an environmenterror [errno 13]
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error `EnvironmentError [Errno 13]` in Python is due to permission issues while trying to install packages.
---

**Contents**

[TOC]

Section 1: Introduction
When working with Python, it is common to encounter errors while trying to install packages. One common error that can be encountered is the "EnvironmentError: [Errno 13]" error. This error typically occurs when the user does not have sufficient permissions to install packages or access certain files.

Section 2: Understanding the Error
The "EnvironmentError: [Errno 13]" error indicates that the Python interpreter does not have permission to access a file or directory that is required for installing a package. This error can occur if the user trying to install the package does not have sufficient permissions to access the system directories or if the file or directory being accessed is currently in use by another process.

Section 3: Solutions to the Error
To solve the "EnvironmentError: [Errno 13]" error, there are several approaches that can be taken. One solution is to run the Python installation with elevated privileges, such as running the command prompt as an administrator. Alternatively, the user can change the permissions of the file or directory being accessed by the Python interpreter. Another solution is to use a virtual environment to install packages, which can help to avoid conflicts with system-level files and directories.

Section 4: Conclusion
In conclusion, encountering the "EnvironmentError: [Errno 13]" error while installing packages in Python can be frustrating, but there are several approaches that can be taken to resolve the issue. By identifying the cause of the error and taking appropriate action, users can successfully install the necessary packages and continue their work with Python.
