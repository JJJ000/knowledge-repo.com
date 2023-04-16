---
title: Installing pip packages into the $home directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: pip can be used to install packages to the user`s home directory by using the --user flag.
---

**Contents**

[TOC]

# Step 1: Install pip

pip is a package manager for Python packages. It can be used to install and manage software packages written in Python. To install pip, follow the instructions on the pip website: https://pip.pypa.io/en/stable/installing/. 

# Step 2: Download Packages

Once pip is installed, you can use it to download packages to your local environment. To do this, open a terminal window and type the command `pip install <package_name>`. This will download the specified package to your current directory. 

# Step 3: Move Packages

Once the packages are downloaded, you can move them to your home folder. To do this, open a terminal window and type the command `mv <package_name> ~/`. This will move the package to your home folder. 

# Step 4: Install Packages

Finally, you can install the packages from your home folder. To do this, open a terminal window and type the command `pip install --user <package_name>`. This will install the package in your home folder.
