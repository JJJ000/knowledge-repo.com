---
title: What are the steps to modify the default Python version?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the command `update-alternatives --config python` in terminal to choose a different version of Python as the default.
---

**Contents**

[TOC]

## Checking the current default Python version

Before changing the default Python version, it is important to first check which version is currently the default. This can be done by opening a command prompt and typing:

```sh
python --version
```

This will display the version number of the default Python interpreter.

## Installing the desired version of Python

If the desired version of Python is not already installed on the system, it will need to be installed. This can be done by downloading the installer from the official Python website and running it.

## Changing the default Python version

Once the desired version of Python is installed, it can be set as the default version by using the update-alternatives command in the terminal. For example, to set Python 3.9 as the default version, run the following command:

```sh
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.9 1
```

This will set Python 3.9 as the default version. To switch back to the previous version, simply run the same command with the path to the previous version of Python.

## Verifying the default Python version

To verify that the default version of Python has been changed, run the following command:

```sh
python --version
```

This should display the version number of the new default Python interpreter. If it does not, try logging out and logging back in, or restarting the system.
