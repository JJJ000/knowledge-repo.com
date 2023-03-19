---
title: Use the pip command to update the Python packages listed in requirements.txt
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the command `pip install -r requirements.txt --upgrade` to upgrade Python packages from requirements.txt using pip.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
The `requirements.txt` file is where you can list all the third-party packages that your Python project depends on. These packages can be easily installed using the `pip` package manager. Upgrading the packages listed in this file is an important task to make sure that your project dependencies are up to date with the latest release versions.

Section 2: Updating pip
-----------------------
Before upgrading the packages, it is best to update the `pip` package manager to the latest version. You can do this by running the following command:

```
pip install --upgrade pip
```

This will upgrade the `pip` package manager to the latest version available.

Section 3: Upgrading packages
-----------------------------
To upgrade the packages listed in the `requirements.txt` file, you can run the following command:

```
pip install --upgrade -r requirements.txt
```

This command will read the `requirements.txt` file and upgrade all the packages listed in it to their latest available versions.

Section 4: Specifying package versions
--------------------------------------
If you want to upgrade specific packages to a certain version, you can modify the `requirements.txt` file accordingly. You can specify the package version by adding the version number after the package name using the format `package_name==version_number`. For example:

```
packageA==1.0.0
packageB>=2.0.0
```

The first line specifies that `packageA` should be installed in version `1.0.0`, while the second line specifies that `packageB` should be installed with a version equal or greater to `2.0.0`. Once you've updated the `requirements.txt` file, you can run the command in section 3 to upgrade the packages.
