---
title: Installing or upgrading from github using conda
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To install/upgrade a package directly from GitHub using conda in Python, use the following command conda install -c conda-forge git+https//github.com/username/repo\_name.git.
---

**Contents**

[TOC]

Introduction to Conda

Conda is an open-source package management system used for software installation, management, and deployment across various operating systems. It can run on Windows, macOS, and Linux. Conda installs and manages packages and their dependencies, resolves package conflicts, and creates and manages isolated environments for different projects.

Installing / Upgrading Conda

To install Conda, first, you need to download and install the software appropriate to the operating system that you are using. Once it is installed, you can use the following command to upgrade Conda to the latest version:

```conda update conda```

You can also use the Anaconda Navigator or the command prompt to update Conda.

Installing / Upgrading Directly from GitHub

Conda allows you to install packages directly from their GitHub repository. To do this, you need to specify the URL of the GitHub repository in the conda install command as follows:

```conda install git+https://github.com/user/repo.git```

Here, user is the username on GitHub, and repo is the name of the repository. You can also specify a specific branch or tag using the following command:

```conda install git+https://github.com/user/repo.git@branch_or_tag```

This will install the package directly from the GitHub repository into your Conda environment.

Conclusion

Conda is a powerful package management system that allows you to install, manage, and deploy packages and their dependencies easily. It also allows you to install packages directly from their GitHub repository, making it easy to work with cutting-edge software that is still in development. With Conda, you can create customized environments for different projects, making it easy to manage dependencies and avoid conflicts.
