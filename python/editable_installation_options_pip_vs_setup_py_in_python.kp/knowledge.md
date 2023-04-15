---
title: Can you rephrase the difference between "pip install --editable ./" and "python setup.py develop"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Both commands are used to install a package in editable mode, but `pip install --editable` is a more modern and recommended approach.
---

**Contents**

[TOC]

# Introduction

In Python, there are different ways to install packages locally. In this article, we will compare two methods that allow us to install a package locally and make changes to it without having to reinstall it every time. These two methods are `pip install --editable ./` and `python setup.py develop`.

# pip install --editable ./

## Definition

`pip install --editable ./` is a command that allows us to install a package locally in "editable" mode. This means that the package is installed in a way that allows us to modify its source code and see the changes immediately without having to reinstall the package.

## How it works

When we run the `pip install --editable ./` command, pip creates a symlink from the installed package to our working directory. This means that any changes we make to the package source code in our working directory will be reflected immediately in the installed package.

## Advantages

One of the key advantages of using `pip install --editable ./` is that it is very easy to use. We simply run the command, and we can start modifying the package source code right away. Another advantage is that it works with pip, which is a widely-used package manager for Python. This means that we can easily uninstall the package, update it, or install other packages that it depends on.

## Disadvantages

One potential disadvantage of using `pip install --editable ./` is that it requires pip. This means that it may not work with other package managers, or with systems that do not have pip installed. Additionally, because it uses a symlink, it may not work on all operating systems or file systems.

# python setup.py develop

## Definition

`python setup.py develop` is a command that allows us to install a package locally in "development" mode. This is similar to the editable mode used by `pip install --editable ./`, in that it allows us to modify the package source code and see the changes immediately.

## How it works

When we run the `python setup.py develop` command, setuptools creates a link between the installed package and the package source code in our working directory. This link allows us to modify the source code directly, and any changes we make will be reflected immediately in the installed package.

## Advantages

One advantage of using `python setup.py develop` is that it works with setuptools, which is another widely-used package manager for Python. This means that we can easily uninstall the package, update it, or install other packages that it depends on. Additionally, because it uses a link instead of a symlink, it may be more compatible with certain file systems.

## Disadvantages

One potential disadvantage of using `python setup.py develop` is that it requires setuptools. This means that it may not work with other package managers, or with systems that do not have setuptools installed. Additionally, because it is less commonly used than `pip install --editable ./`, it may be less well-documented and less well-supported.

# Conclusion

Both `pip install --editable ./` and `python setup.py develop` are useful tools for installing packages locally in a way that allows us to modify the source code and see the changes immediately. The choice between them will depend on the specific needs of the project, as well as the package manager and file system being used. In general, `pip install --editable ./` may be more widely-used and easier to use, while `python setup.py develop` may be more compatible with certain systems and file systems.
