---
title: The command "pipenv" was not found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The issue of `Pipenv` command not found in Python can be resolved by installing the `pipenv` module using pip.
---

**Contents**

[TOC]

# Overview

Pipenv is a dependency manager for Python virtual environments. It helps to manage package dependencies and versions for Python projects. However, sometimes when you try to run pipenv command, it throws an error "command not found". This can be a common error and is usually due to incorrect installation or setup issues. This guide will walk you through various solutions to fix the "pipenv command not found" error in Python.

# Solution 1: Reinstall Pipenv

The "pipenv command not found" error can be due to a corrupted or incomplete installation of Pipenv. In this case, reinstalling Pipenv can help to fix the issue. Follow the below steps to reinstall Pipenv.

1. Uninstall Pipenv by running the following command in the terminal:
   `pip uninstall pipenv`
2. Once uninstalled, install Pipenv again using the command:
   `pip install pipenv`
3. After installation, verify Pipenv is installed by running the command:
   `pipenv` or `pipenv help`

# Solution 2: Add Pipenv to System Path

If Pipenv is installed but you are still getting the "pipenv command not found" error, it could be because Pipenv is not added to the system path. Follow the below steps to add Pipenv to the system path.

1. Find the installation path of Pipenv by running the command:
   `pipenv --venv`
2. Once you get the installation path, copy it.
3. Open the terminal and type the command `sudo nano /etc/paths`
4. Enter your password when prompted.
5. Add the copied path to the end of the file and press control + X to save the changes.

```
/usr/local/bin
/usr/bin
/bin
/usr/sbin
/sbin
/Users/Username/.local/share/virtualenvs/pipenv-*****
```

6. Restart the terminal and run the command `pipenv` to check if the command not found error is resolved.

# Solution 3: Use Virtual Environments

Another solution to the "pipenv command not found" error is to use virtual environments. Virtual environments are isolated environments that have their own Python installations and package dependencies. By using virtual environments, you can avoid issues related to the system path and package conflicts.

1. Create a new virtual environment by running the command:
   `python -m venv myenv`
2. Activate the virtual environment using the command:
   `source myenv/bin/activate`
3. Install Pipenv inside the virtual environment using the command:
   `pip install pipenv`
4. Once installed, verify Pipenv is installed by running the command:
   `pipenv` or `pipenv help`.

# Conclusion

The "pipenv command not found" error is usually caused by incorrect installation or setup issues. The above solutions can help you resolve the issue and use Pipenv for your Python projects. Reinstalling Pipenv, adding Pipenv to the system path or using virtual environments are some of the ways to resolve the "pipenv command not found" error.
