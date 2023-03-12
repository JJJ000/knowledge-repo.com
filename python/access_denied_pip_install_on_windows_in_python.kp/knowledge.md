---
title: Access denied while attempting to install pip on a windows system
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Try running the command prompt as administrator and then run the `pip install` command again.
---

**Contents**

[TOC]

Section 1: Introduction

When working with Python, you may come across a scenario where you need to install a package using the pip package installer. However, sometimes you may encounter an error message like "access denied" on Windows. This error message indicates that your user account does not have the necessary permissions to install packages using the pip package installer. In this guide, we will discuss some of the possible reasons why you may encounter this error message and provide some solutions to fix it.

Section 2: Common Causes of Access Denied Error on Windows

There are several reasons why you may encounter the "access denied" error when trying to install a package using pip on Windows. Some of the most common causes of this error message include:

1. User Account Control (UAC) Restrictions: If your user account does not have administrative rights on your Windows computer, you may encounter this error message when trying to install packages using pip.

2. Antivirus Software: Some antivirus programs may prevent you from installing packages using pip. This is because some packages downloaded by pip may be flagged as potential threats.

3. File System Permissions: If the directory where pip is installed or the directory where the package is being installed does not have the correct file system permissions, you may encounter an access denied error when using pip.

Section 3: Solutions to Fix Access Denied Error on Windows

Here are some possible solutions you can try to fix the "access denied" error when using pip on Windows:

1. Run pip as Administrator: You can try running pip as an administrator to bypass any UAC restrictions. To do this, open the command prompt as an administrator and type "pip install package_name" to install the package.

2. Disable Antivirus Software: If you suspect that your antivirus software is preventing you from installing the package, you can try disabling it temporarily and then run pip again to see if the error is resolved.

3. Change File System Permissions: If the error is caused by file system permissions, you can try giving your user account permission to the directory where pip is installed or the directory where the package is being installed. You can do this by right-clicking on the directory, selecting Properties, navigating to the Security tab, and adding your user account with Full Control permission.

4. Use a Virtual Environment: Another solution is to use a virtual environment. A virtual environment is an isolated environment where you can install packages without affecting the global Python installation. To create a virtual environment, you can use the command "python -m venv myenv" in the command prompt. This will create a virtual environment named "myenv" in the current directory. You can then activate the virtual environment using the command "myenv\Scripts\activate". Once the virtual environment is activated, you can use pip to install packages without encountering any access denied errors.

Section 4: Conclusion

In this guide, we have discussed some of the common causes of the "access denied" error when using pip on Windows and provided some possible solutions to fix it. By following these solutions, you should be able to install packages using pip without encountering any access denied errors.
