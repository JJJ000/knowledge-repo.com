---
title: What packages have been installed using easy_install/pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The command `pip freeze` can be used to list all packages installed with easy\_install/pip in Python.
---

**Contents**

[TOC]

#### Using easy_install

The `easy_install` command can be used to install packages from the Python Package Index (PyPI) and other indexes. The command can be used to list all packages installed with `easy_install` by running the following command:

```
easy_install --local
```

This command will list all packages installed with `easy_install` in the current environment.

#### Using pip

The `pip` command is a more modern and user-friendly alternative to `easy_install`. It can also be used to install packages from PyPI and other indexes. The command can be used to list all packages installed with `pip` by running the following command:

```
pip list
```

This command will list all packages installed with `pip` in the current environment.
