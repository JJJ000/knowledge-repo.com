---
title: What is the process for installing a Python package using a .whl file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Install the package by running `pip install filename.whl` in the command line.
---

**Contents**

[TOC]

# Prerequisites

Before attempting to install a Python package with a .whl file, ensure that the version of Python installed on your machine is compatible with the version of the package you are trying to install.

# Installing With `pip`

The easiest way to install a Python package with a .whl file is to use the `pip` command. To do this, navigate to the directory where the .whl file is located and run the following command:

```
pip install package_name.whl
```

# Installing With `easy_install`

Alternatively, you can use the `easy_install` command to install a Python package with a .whl file. To do this, navigate to the directory where the .whl file is located and run the following command:

```
easy_install package_name.whl
```

# Installing With `wheel`

Finally, you can use the `wheel` command to install a Python package with a .whl file. To do this, navigate to the directory where the .whl file is located and run the following command:

```
wheel install package_name.whl
```
