---
title: How to install Python 3 on rhel?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can install Python 3 on RHEL by running the command `sudo yum install python3`.
---

**Contents**

[TOC]

## Section 1: Update System Packages

Before installing any new software, it's important to update your system packages to ensure that you have the latest security fixes and critical updates. To do this on RHEL, run the following command:

```
sudo yum update
```

You may need to enter your administrator password to authorize the update process. Wait for the update to complete before moving on to the next section.


## Section 2: Install Python 3

Once your system is up to date, you can install Python 3 using yum. Run the following command:

```
sudo yum install python3
```

This will download and install the latest version of Python 3 from the official RHEL repositories. Wait for the installation to complete before moving on to the next section.


## Section 3: Verify Python 3 Installation

To verify that Python 3 has been installed successfully, run the following command:

```
python3 --version
```

This should output a message indicating the version of Python 3 that is now installed on your system. If you see an error message or if the version number is not what you expected, you may need to try reinstalling Python 3 or seeking additional help from the RHEL community.

## Section 4: Additional Packages and Libraries

With Python 3 installed, you may also want to install additional packages and libraries to support your development projects. These can be installed using the pip package management system, which should be included with your Python 3 installation.

To install a package or library using pip, run a command like this:

```
pip3 install package-name
```

Replace "package-name" with the name of the package or library that you want to install. Note that some packages may have additional dependencies or installation requirements, so be sure to read the documentation carefully before beginning the installation process.
