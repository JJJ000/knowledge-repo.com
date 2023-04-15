---
title: When attempting to install pillow on alpine linux, an error message appears stating that "limits.h" file or directory does not exist
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The package containing `limits.h` is missing in Alpine Linux, so it needs to be installed manually with `apk add --no-cache linux-headers`.
---

**Contents**

[TOC]

### Introduction
Pillow is a popular Python library that provides support for opening, manipulating, and saving many different image file formats. If you're running Alpine Linux and trying to install Pillow in Python, you may encounter an error that says "No such file or directory 'limits.h'". In this guide, we'll explain why this error occurs and how you can fix it.

### Understanding the Error
The "limits.h" file is a system header file that defines various constants and limits used by the C standard library and other system libraries. When you try to install Pillow in Python on Alpine Linux, the installation process may attempt to compile some C code that uses the limits.h header. However, the limits.h file may not be present on your Alpine Linux system, causing the installation to fail with the "No such file or directory" error message.

### Fixing the Error
To fix the "No such file or directory 'limits.h'" error when installing Pillow on Alpine Linux in Python, you can try installing the libc-dev package, which provides the limits.h file and other C standard library headers. Here's how:

1. Open a terminal window and log in to your Alpine Linux system.
2. Run the following command to install the libc-dev package:

   ```
   apk add libc-dev
   ```

3. Wait for the installation to complete.
4. Try installing Pillow in Python again by running the command `pip install pillow`.

With the libc-dev package installed, the installation process should be able to find the limits.h file and complete without errors.

### Conclusion
If you're encountering the "No such file or directory 'limits.h'" error when installing Pillow on Alpine Linux in Python, it's likely due to a missing system header file. By installing the libc-dev package, you can provide the necessary headers and resolve the error. We hope this guide has been helpful in resolving this issue.
