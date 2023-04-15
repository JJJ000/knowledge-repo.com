---
title: Although pip successfully installs packages, executable files cannot be located from the command line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The PATH environment variable may not be set properly to include the location of the executable.
---

**Contents**

[TOC]

# Overview

When you install a Python package using pip, it should automatically add the package's executables to your PATH environment variable. However, sometimes the executables are not found from the command line after installation, even though pip reported a successful installation. This can be frustrating, but there are a few solutions to this problem.


## Double Check the PATH Environment Variable

First, you should double check that the package's executables were added to your PATH environment variable. You can do this by running the following command in your command prompt:

```
echo %PATH%
```

This will print out a list of directories that are included in your PATH. Look for the directory that corresponds to the package you installed (e.g., if you installed the requests package, you should look for a directory containing a file called "requests.exe" or similar). If you don't see the directory in your PATH, you can add it manually using the following command:

```
set PATH=%PATH%;C:\path\to\package\executables
```

Be sure to replace "C:\path\to\package\executables" with the actual path to the directory containing the package's executables.


## Check for a Scripts Directory

In some cases, the executables may be installed in a "Scripts" directory rather than being added to your PATH directly. You can check for this by looking in the site-packages directory where the package is installed. This directory should be located in your Python installation directory (e.g., C:\PythonXX\Lib\site-packages\package_name). If you see a "Scripts" directory here, try adding it to your PATH using the command in the previous section.

```
set PATH=%PATH%;C:\path\to\package\scripts
```

If the package has multiple executables, you may need to add the "Scripts" directory and its subdirectories to your PATH to ensure that all of the executables are available.


## Reinstall the Package

If the above solutions don't work, you can try reinstalling the package using the --user flag:

```
pip install package_name --user
```

This will install the package for the current user only, rather than installing it for all users on the system. In some cases, this can resolve issues with the package's executables not being found.


## Summary

In summary, if you're having trouble with executable files not being found after installing a Python package, you can try checking the PATH environment variable, looking for a Scripts directory, or reinstalling the package using the --user flag. Hopefully one of these solutions will work for you!
