---
title: Verify whether the Python package has been installed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the command `pip freeze` to list all installed packages in Python.
---

**Contents**

[TOC]

## Option 1: Using pip list command

One way to check if a Python package is installed on your system is to use the pip list command. This command lists all the packages that are installed on your system. To check if a specific package is installed, simply search for its name in the list.

```
pip list | grep <package_name>
```

For example, to check if the numpy package is installed, run the following command:

```
pip list | grep numpy
```

If the package is installed, you will see its name and version number in the output.

## Option 2: Trying to import the package

Another way to check if a Python package is installed is to try to import it in a Python script or interactive shell. If the package is installed, it will be imported successfully without any errors.

```
import <package_name>
```

For example, to check if the numpy package is installed, open a Python shell and run the following command:

```
import numpy
```

If the package is installed, the command will run without any errors. If the package is not installed, you will see an error message like "ModuleNotFoundError: No module named 'numpy'".

## Option 3: Checking the installed packages directory

Finally, you can also check if a Python package is installed by looking for its directory in the installed packages directory. This directory contains all the packages that are installed using pip or other package managers.

The installed packages directory can vary depending on your system configuration and Python version. Here are the common locations for the installed packages directory:

- Windows: `C:\PythonXX\Lib\site-packages\`
- macOS and Linux: `/usr/local/lib/pythonXX/site-packages/` or `/usr/lib/pythonXX/site-packages/`

Replace `XX` with the Python version number (e.g. `3.9`).

Once you have found the installed packages directory, you can look for the package directory inside it. The package directory will have the same name as the package. If the directory is present, the package is installed. If the directory is not present, the package is not installed.

For example, to check if the numpy package is installed on a Linux system with Python 3.9 installed, run the following command:

```
ls /usr/local/lib/python3.9/site-packages | grep numpy
```

If the package is installed, you will see its directory name in the output. If the package is not installed, there will be no output.
