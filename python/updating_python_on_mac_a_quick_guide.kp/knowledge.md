---
title: How to update Python on a mac
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To update Python on a Mac, use the terminal command `brew install python3` to install the latest version of Python 3 using Homebrew.
---

**Contents**

[TOC]

# Checking the Current Version of Python 

The first step in updating Python on a Mac is to check the current version of the programming language. This can be done by opening the Terminal application and typing the following command:

```python --version``` 

This will display the currently installed version of Python on the Mac.

# Using Homebrew to Update Python 

Homebrew is a package manager for MacOS that allows users to easily install and update software packages. To update Python using Homebrew, follow these steps:

1. Open Terminal application and run the following command to install Homebrew:
   ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
   
2. After Homebrew is installed, run the following command to update the Homebrew packages:
   ```brew update```
   
3. Once the packages are updated, run the following command to update Python:
   ```brew upgrade python```
   
4. Homebrew will then start downloading and installing the latest version of Python. It may take some time to complete.

# Using the Python Website to Update Python

Another way to update Python on a Mac is to download the latest installer from the official website. Follow these steps:

1. Go to [https://www.python.org/downloads/mac-osx/](https://www.python.org/downloads/mac-osx/) in a web browser.

2. Download the latest version of Python for Mac OS X.

3. Open the downloaded package and follow the installation instructions.

4. Once the installation is complete, the latest version of Python should be available for use.

# Verifying the Updated Version of Python 

After updating Python on a Mac, it is recommended to verify that the process was completed successfully. This can be done by once again checking the current version of Python using the command:

```python --version``` 

If the latest version of Python is displayed, then the update was successful.
