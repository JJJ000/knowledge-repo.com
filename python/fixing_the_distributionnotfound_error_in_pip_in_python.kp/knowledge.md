---
title: How can I resolve the distributionnotfound error when pip is not functioning correctly?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Reinstall the package with pip install package-name, replacing `package-name` with the name of the missing package.
---

**Contents**

[TOC]

## Introduction
The "DistributionNotFound" error in Python happens when a package that the script needs is not installed or is not found in the Python path. This error occurs when trying to run a script, execute a command or when importing a package. This error is more common in virtual environments when the package is not installed inside the virtual environment.

## Troubleshooting steps
Here are a few steps to fix the "DistributionNotFound" error in Python:

### Step 1: Check if the package is installed
The first thing to do when encountering a "DistributionNotFound" error is to check if the package is installed. You can use the pip command to check if a package is installed:

```
pip list | grep package_name
```

This command will list all the installed packages and check if the specified package is installed. If the package is not installed, then you will need to install it using the pip command:

```
pip install package_name
```

### Step 2: Check the Python path
If the package is installed but the error persists, then the package might not be installed in the Python path. You can check the Python path by running the following command:

```
python -c "import sys; print(sys.path)"
```

This command will print the list of directories where Python will look for packages. Make sure that the directory containing the package is in the list of directories.

### Step 3: Reinstall the package
If the package is installed and in the Python path, then it might be a problem with the package installation. You can try reinstalling the package:

```
pip uninstall package_name
pip install package_name
```

This will uninstall the package and install it again.

### Step 4: Check the virtual environment
If you are using a virtual environment, then the package might not be installed inside the virtual environment. Make sure that you activate the virtual environment and then install the package:

```
source path/to/virtual/environment/bin/activate
pip install package_name
```

## Conclusion
The "DistributionNotFound" error in Python can be fixed by checking if the package is installed, checking the Python path, reinstalling the package or checking the virtual environment. If these steps do not work, then it might be an issue with your system configuration or the package itself.
