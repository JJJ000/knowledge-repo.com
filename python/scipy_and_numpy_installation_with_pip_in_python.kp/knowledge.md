---
title: The process of using pip to install numpy and scipy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To install SciPy and NumPy using pip in Python, use the command `pip install numpy scipy`.
---

**Contents**

[TOC]

Installation of pip

Before installing SciPy and NumPy using pip, you need to ensure that pip is installed on your computer. pip is the package installer for Python. Here are the steps to install pip:

1. Go to the Python website and download the latest version of Python.
2. During the installation process, make sure to select the "Add Python to PATH" option.
3. Finally, open the command prompt and type "pip" to check if pip is installed. 

If pip is not installed, download the pip installer from https://bootstrap.pypa.io/get-pip.py and run it using the following command in the Command Prompt: 

```
python get-pip.py
```


Installation of NumPy and SciPy using pip

Once you have pip installed on your computer, you can easily install NumPy and SciPy by following these steps: 

1. Open the Command Prompt or Terminal on your computer.
2. Type the following command in the Command Prompt for installing NumPy: 

```
pip install numpy
```

3. Wait for the installation to complete. 
4. Finally, type the following command for installing SciPy: 

```
pip install scipy
```
5. Wait for the installation to complete. 
6. Finally, to verify that NumPy and SciPy have been installed correctly, type the following command: 

```
import numpy
import scipy
``` 

If there are no errors, then both libraries are installed correctly.
