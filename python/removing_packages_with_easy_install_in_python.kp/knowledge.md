---
title: What is the process for uninstalling packages that were installed using python's easy_install?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the command `easy\_install -m <package\_name>` to remove packages installed with Python`s easy\_install.
---

**Contents**

[TOC]

# Uninstalling Packages

## Step 1: Find the Package Name

The first step in uninstalling a package installed with easy_install is to find the package name. To do this, you can use the easy_install command with the -m flag, which will list all the packages that have been installed with easy_install.

For example, to list all the packages installed with easy_install, you can run the following command:

```
easy_install -m
```

This will list all the packages installed with easy_install, along with their version numbers.

## Step 2: Uninstall the Package

Once you have the package name, you can use the easy_install command with the -u flag to uninstall the package.

For example, to uninstall a package named mypackage, you can run the following command:

```
easy_install -u mypackage
```

This will uninstall the package from your system.

## Step 3: Confirm Uninstall

You can confirm that the package has been successfully uninstalled by running the easy_install command with the -m flag again. This should no longer list the package that you just uninstalled.

For example, to confirm that the package mypackage has been uninstalled, you can run the following command:

```
easy_install -m
```

If the package is no longer listed, then it has been successfully uninstalled.
