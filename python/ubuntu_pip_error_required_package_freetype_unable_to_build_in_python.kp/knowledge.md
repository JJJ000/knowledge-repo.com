---
title: An error message is displayed while running 'pip install' on ubuntu, stating that the package cannot be built which is mandatory for functioning - the package in question is freetype
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You need to install the development packages for freetype before running the `pip install` command.
---

**Contents**

[TOC]

## Background

Pip is a package manager for Python that allows users to easily install, upgrade, and manage Python modules. In some cases, when using pip to install certain packages, you may encounter errors when attempting to build or install required dependencies. One such error that may occur when running `pip install` in Ubuntu is the error message: 

`The following required packages can not be built: * freetype`

In this case, the error message is indicating that the package freetype is a required dependency for the package you are attempting to install, but it cannot be built successfully.

## Troubleshooting Steps

1. Check that freetype is installed:
   - First, make sure that freetype is installed on your system. You can do this by running the following command in your terminal:
     ```
     dpkg -s libfreetype6-dev
     ```
     If freetype is not installed, you can install it using the following command:
     ```
     sudo apt-get install libfreetype6-dev
     ```

2. Check that other dependencies are installed:
   - If freetype is installed, but you are still encountering the error message, it is possible that there are other missing dependencies that are required for freetype to build successfully. You can check if there are any missing dependencies by running the following command:
     ```
     sudo apt-get build-dep python-matplotlib
     ```
     This command will install any missing dependencies for the python-matplotlib package. If this command succeeds, you should be able to run `pip install` for the package you are trying to install without encountering the previous error message.

3. Try reinstalling the package:
   - If you are still encountering the error message after verifying that freetype is installed and checking for other missing dependencies, you may want to try reinstalling the related package. This can be done using the following command:
     ```
     pip install --reinstall <package_name>
     ```
     This command will attempt to reinstall the package and all of its dependencies from scratch. If a failed installation or missing dependency was causing the issue, this may be enough to resolve the error message.

4. Consider using a virtual environment:
   - If none of the previous steps have resolved the error message, it is possible that conflicting dependencies or configurations on your system are causing the issue. In this case, you may want to try using a virtual environment to install and manage your Python modules. This can help to isolate your Python environment from your system environment and prevent conflicts between packages. You can create a virtual environment using the following commands:
     ```
     sudo apt-get install python3-venv
     python3 -m venv myenv
     source myenv/bin/activate
     ```
     This will create a new virtual environment named 'myenv' and activate it. You can then install your desired packages within the virtual environment using pip.
