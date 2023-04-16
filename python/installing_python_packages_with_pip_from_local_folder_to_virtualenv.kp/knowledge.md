---
title: Using pip to install Python packages from a local file system folder into a virtualenv
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can install Python packages from a local file system folder to a virtualenv with pip by using the `pip install -r /path/to/requirements.txt` command.
---

**Contents**

[TOC]

# Section 1: Create a Virtual Environment

The first step is to create a virtual environment in which to install the Python packages from the local file system folder. This can be done by using the `virtualenv` command. This will create a new directory containing the environment, which can then be activated by running the `source` command.

# Section 2: Install Packages

Once the virtual environment has been created, the Python packages can be installed using the `pip` command. This command will search the local file system folder for packages and install them into the virtual environment.

# Section 3: Activate Environment

After the packages have been installed, the virtual environment needs to be activated. This can be done by running the `source` command and passing in the path to the environment directory. This will ensure that the packages installed in the virtual environment are used when running Python.

# Section 4: Verify Installation

The final step is to verify that the packages have been successfully installed. This can be done by running the `pip list` command, which will list all of the packages installed in the virtual environment. If the packages from the local file system folder are present, then the installation was successful.
