---
title: What's the process for installing Python 2 and 3 on a mac using homebrew?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the commands `brew install python` for Python 2 and `brew install python3` for Python 3.
---

**Contents**

[TOC]

### Section 1: Install Homebrew

Before we can use Homebrew to install Python 2 and 3, we need to have Homebrew installed on our Mac. To install Homebrew, open Terminal and run the following command:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

This command will download and install Homebrew on your Mac.

### Section 2: Install Python 2 and 3 with Homebrew

Once we have Homebrew installed, we can use it to install Python 2 and 3. To do this, open Terminal and run the following commands:

```
brew install python@2
brew install python
```

The first command installs Python 2, while the second command installs Python 3.

### Section 3: Verify Python 2 and 3 installation

To verify that both Python 2 and 3 have been installed correctly, run the following commands in Terminal:

```
python2 --version
python3 --version
```

These commands should display the version of Python 2 and 3 that you have installed, respectively.

### Section 4: Using Python 2 and 3

Now that we have Python 2 and 3 installed, we can use them in our projects. To use Python 2, we can simply run the following command in Terminal:

```
python2 my_script.py
```

To use Python 3, we can use the following command:

```
python3 my_script.py
```

Here, `my_script.py` is the name of the Python script that we want to run.
