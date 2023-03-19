---
title: How is 'python setup.py install' different from 'pip install'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Both commands can install Python packages, but `pip install` is recommended because it handles dependencies and updates more efficiently.
---

**Contents**

[TOC]

Overview

Both 'python setup.py install' and 'pip install' are used to install Python packages. However, there are some distinct differences between these two methods. In this article, we will discuss these differences in detail.

Section 1: Source vs. Binary Distribution

The primary difference between 'python setup.py install' and 'pip install' lies in the way they install packages. 'python setup.py install' works by compiling the source code of the package and then installing it. In other words, it installs the package from the source distribution. On the other hand, 'pip install' installs the package from a binary distribution. Binary distributions are pre-compiled packages that are ready to install.

Section 2: Package Dependencies

Another significant difference between the two methods is how they handle package dependencies. When you use 'python setup.py install,' it only installs the package you are trying to install. It does not install any dependencies required by that package. If you want to install the dependencies, you will have to do that manually. Conversely, 'pip install' automatically installs all the dependencies required by a package.

Section 3: Version Control

When you install a package using 'python setup.py install,' you do not have any control over the version of the package that gets installed. It will always install the latest version available on your system. On the other hand, 'pip install' allows you to specify the version of the package you want to install. This feature is especially useful when testing an application that is sensitive to the package version.

Section 4: Package Removal

Finally, when it comes to package removal, 'python setup.py install' can be a little tricky to remove. It is because the installation process does not create any metadata files that tell you where the package has been installed. Removing the package will involve searching for and removing all the individual files manually. Conversely, 'pip uninstall' can easily remove any package installed with pip.

Conclusion

In conclusion, 'python setup.py install' and 'pip install' are both useful methods for installing Python packages. However, they have distinct differences in how they install packages, manage package dependencies, version control, and package removal. The choice of which method to use depends on the developer's specific needs and use case.
