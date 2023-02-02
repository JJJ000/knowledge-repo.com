---
title: What is the difference between running 'python setup.py develop' and 'python setup.py install' in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: `setup.py develop` will install a link to the source code, while `setup.py install` will install the package in the system`s Python site-packages directory.
---

**Contents**

[TOC]

# Setup.py Install

The `setup.py install` command is used to install a Python package from source. This command builds the package from source and copies the resulting files to the appropriate location on the user's system. This command is typically used when installing a package from a source code repository, such as a Git repository.

# Setup.py Develop

The `setup.py develop` command is used to install a Python package in "development mode". This command builds the package from source and creates a link between the source files and the installed files. This allows the user to make changes to the source code and have those changes reflected in the installed version of the package. This command is typically used when developing a package, as it allows changes to be made to the source code without having to reinstall the package.
