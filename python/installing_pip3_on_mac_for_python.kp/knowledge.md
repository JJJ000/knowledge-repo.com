---
title: What is the process to install pip3 for Python on a mac?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can install Python`s pip3 on your Mac by running the command `sudo easy\_install pip3` in Terminal.
---

**Contents**

[TOC]

### Introduction
Pip is a package management system used to install and manage software packages written in Python. In this tutorial, we will explain how to install pip3 on a Mac.

### Prerequisites
Before you can begin installing pip3 on your Mac, you should have the following:

- A Mac running macOS X or later
- Administrative access to your computer
- Access to a terminal program (such as Terminal, iTerm, or XTerm)

### Step 1: Install Homebrew

Homebrew is a package manager for macOS that makes it easy to install software packages. Here's how to install Homebrew:

1. Open your terminal and paste the following command:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2. Press Enter and wait for the installation to complete.

### Step 2: Install Python

Python comes pre-installed with macOS, but we need to install it using Homebrew to ensure that we have the latest version. Here's how to install Python:

1. Open a terminal and run the following command:

```
brew install python
```

2. Press Enter and wait for the installation to complete.

### Step 3: Install pip3

Now that we have Python installed, we can use its package manager, pip, to install pip3. Here's how:

1. Open a terminal and run the following command:

```
sudo easy_install pip3
```

2. You'll be prompted to enter your password. Enter it and press Enter.

3. Wait for the installation to complete. Once it's done, pip3 will be installed on your Mac.

### Conclusion
By following these simple steps, you should now have pip3 installed on your Mac. You can now use it to install Python packages and libraries to help you with your Python programming projects.
