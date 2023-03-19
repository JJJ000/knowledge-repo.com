---
title: What are the steps to install an older version of Python 3 on macos using homebrew?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To install a previous version of Python 3 using homebrew on macOS, run the command `brew install python@3.x` (replace x with the desired version number).
---

**Contents**

[TOC]

## **Section 1: Installing Homebrew**

Homebrew is a popular package manager for macOS that makes it easy to install software like Python. To install Homebrew on your Mac, follow these steps:

1. Open Terminal, which is located in the Utilities folder within your Applications folder.

2. Install Homebrew by running the following command in your terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Press enter, and you will be asked to enter your password.

4. After entering your password, the installation process will begin. Wait for the installation to complete.

5. After the installation is complete, confirm that Homebrew is working by running the following command:
```
brew --version
```

## **Section 2: Finding the version of Python you want to install**

Before installing a previous version of Python, you first need to know which version you want to install. You can find a list of all available versions of Python by running the following command in your terminal:
```
brew search python@3
```

This will give you a list of all the available versions of Python that you can install. Look through the list and find the version that you want to install.

## **Section 3: Installing the previous version of Python**

After finding the version of Python you want to install, you can install it using the following command:
```
brew install python@<version_number>
```

For example, if you want to install Python 3.7.10, you would run the following command:
```
brew install python@3.7.10
```

Wait for the installation to complete, and you're done!

## **Section 4: Verifying the installation**

To confirm that the installation was successful, you can run the following command in your terminal to check the version of Python installed:
```
python3 --version
```

If you see the version number that you installed, then you have successfully installed the previous version of Python using Homebrew.
