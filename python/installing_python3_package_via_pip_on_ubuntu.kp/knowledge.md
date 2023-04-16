---
title: What is the process for using pip to install the python3 version of a package on ubuntu?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run `pip3 install <package\_name>` to install the python3 version of a package via pip on Ubuntu.
---

**Contents**

[TOC]

### Step 1: Update pip

Before installing a package, it is important to update pip to the latest version. This can be done by running the command:

```
sudo apt-get install python3-pip
```

### Step 2: Install the package

Once pip is updated, the package can be installed using the command:

```
pip3 install <package-name>
```

### Step 3: Check the installation

To check that the package has been installed correctly, run the command:

```
pip3 list
```

This will list all the packages installed via pip. The newly installed package should be in the list.

### Step 4: Verify version

To verify the version of the package installed, run the command:

```
pip3 show <package-name>
```

This will display the version of the package installed.
