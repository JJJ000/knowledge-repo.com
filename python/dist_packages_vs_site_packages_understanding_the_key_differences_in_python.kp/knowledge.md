---
title: Could you elaborate on the distinctions between dist-packages and site-packages?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: site-packages contains third-party modules, while dist-packages contains modules installed as part of a Debian package.
---

**Contents**

[TOC]

## Overview
In Python, libraries, modules, and packages can be installed either in dist-packages or site-packages. These folders hold the installed packages that are used by the interpreter in a different way. Here are some of the differences between the two.

## Location
Dist-packages and site-packages are folders that are located at different paths in the system.

Dist-packages are used by the Linux package manager, which installs system-level packages. The packages installed via package managers, such as apt-get or yum, are stored in the dist-packages directory. It is usually located at /usr/lib/python<version>/dist-packages.

Site-packages on the other hand, refers to the collection of third-party packages installed using other tools like pip or easy-install. These packages are installed by a user or a developer at a system-level or virtual environment level. Site-packages is usually located at /usr/lib/python<version>/site-packages.


## Priority
When Python imports a module, it searches in different directories, in a specific order, to find the required module. Site-packages has higher priority over dist-packages in terms of the order of the search. As such, any packages installed in site-packages will be given higher priority than those in dist-packages.

## Deleting Packages
Deleting packages in dist-packages can cause major problems in the system because the package management system relies on that directory. Removing a package manually can result in issues with upgrading or removing the package later.

On the other hand, deleting packages in site-packages should not cause any issues to the system, since these packages are user-level packages and are not managed by the package management system.



So, in summary, dist-packages contains system-level packages that the package manager controls, while site-packages contains user-level packages that are installed via other tools like pip. The order of the directory search is different, so packages installed in site-packages have a higher priority than those in dist-packages. Removing packages from dist-packages manually can be problematic, whereas removing packages from site-packages should not cause any issues.
