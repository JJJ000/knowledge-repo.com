---
title: What is the process for globally installing a pip package instead of locally?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the command `pip install PACKAGE\_NAME --user` to install a package locally or `sudo pip install PACKAGE\_NAME` to install it globally.
---

**Contents**

[TOC]

Installing Pip Packages Globally in Python

Python packages installed via pip are typically installed locally in a user's home directory. This is done to avoid conflicts between different Python versions or different package versions. However, there may be cases where you want to install a package globally on your system, so that it can be used by all users and Python installations. Here's how to do that:

Section 1: Upgrade pip

Before installing a package globally, it's a good idea to ensure that your pip installation is up to date. This can be done with the following command run in your terminal:

```
pip install --upgrade pip
```

Section 2: Install the package globally

To install a package globally, you simply need to add the `sudo` command to the front of the pip command. This will give pip superuser privileges and allow it to install the package in a global location. Here's the command:

```
sudo pip install package_name
```

Replace "package_name" with the actual name of the package you want to install globally.

Section 3: Verify the package is installed globally

To verify that the package is installed globally, you can use the `pip show` command. This will show you the package information, including the location where it was installed. Here's the command:

```
pip show package_name
```

Again, replace "package_name" with the actual name of the package you installed globally.

Section 4: Uninstall a globally installed package

To uninstall a globally installed package, you again need to use the `sudo` command to give pip superuser privileges. Here's the command:

```
sudo pip uninstall package_name
```

Replace "package_name" with the actual name of the package you want to uninstall globally.

And that's it! By following these simple steps, you can easily install pip packages globally in Python.
