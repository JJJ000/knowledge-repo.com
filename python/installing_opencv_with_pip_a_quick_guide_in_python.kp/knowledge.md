---
title: Can you guide me on installing opencv through pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To install OpenCV using pip in Python, run the command `pip install opencv-python` in the terminal or command prompt.
---

**Contents**

[TOC]

# Installing OpenCV using pip in Python

Here are the steps to install OpenCV using pip in Python:

## Step 1: Check the Python version

Before installing OpenCV, you need to check the version of Python installed on your system. Open a command prompt and enter the following command:

```
python --version
```

If your version is less than 2.0 or 3.0, then you should update your Python version to the latest one.


## Step 2: Install pip

pip is a package installation tool used to install and manage Python packages. It comes pre-installed with Python 2.7.9+ and Python 3.4+, so you do not need to install pip for those versions. However, if you have a lower version of Python, you will need to install pip.

To install pip, open a command prompt and enter the following command:

```
sudo apt-get install python-pip
```

## Step 3: Install OpenCV

Once pip is installed, you can now install OpenCV using the following command:

```
pip install opencv-python
```

If you need the additional modules that come with OpenCV, you can install them using the following command:

```
pip install opencv-contrib-python
```

That's it! OpenCV is now installed on your system and you can start using it.
