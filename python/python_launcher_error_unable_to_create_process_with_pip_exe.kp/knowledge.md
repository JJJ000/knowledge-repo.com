---
title: The launcher encountered a fatal error and could not create a process using the specified file path for Python and pip in the program files directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The launcher is unable to create a process using the specified Python and pip executable paths.
---

**Contents**

[TOC]

Section 1: Introduction
When attempting to install or upgrade packages using `pip`, you may encounter a `Fatal error in launcher` message followed by `Unable to create process using ""C:\Program Files (x86)\Python33\python.exe" "C:\Program Files (x86)\Python33\pip.exe""`. This error indicates that the Python interpreter was unable to launch the specified `pip` executable.

Section 2: Possible Causes
There are several possible causes for this error, including:
- A corrupted or incomplete Python installation
- A mismatch between the Python and pip versions
- An issue with the program or script attempting to use `pip`

Section 3: Troubleshooting Steps
To resolve this error, you can try the following troubleshooting steps:
1. Ensure that both Python and `pip` are installed correctly and their paths are properly configured in your system environment variables.
2. Verify that your Python and `pip` versions are compatible. You can check the version of Python by running the command `python --version`, and for pip, `pip --version`.
3. If the above steps do not resolve the issue, try using the `python -m pip` command instead of the standalone `pip` command.
4. If you are running a script, try running it with administrative privileges or modifying the script to specify the full path to the `pip` executable.

Section 4: Conclusion
The `Fatal error in launcher: Unable to create process using ""C:\Program Files (x86)\Python33\python.exe" "C:\Program Files (x86)\Python33\pip.exe""` error can be frustrating when attempting to use the `pip` package manager. However, by following the troubleshooting steps outlined above, you can resolve this issue and continue installing and upgrading packages as needed.
