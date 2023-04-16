---
title: Unable to successfully install the Python cryptography package using both pip and setup.py
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is possible that the installation failed due to incompatibilities with the operating system or other installed packages.
---

**Contents**

[TOC]

#### Using PIP

1. Check if PIP is installed: 
    - Open a command prompt window and type `pip --version`. 
    - If PIP is not installed, follow the instructions [here](https://pip.pypa.io/en/stable/installing/) to install it.

2. Install the Cryptography package: 
    - Open a command prompt window and type `pip install cryptography`. 
    - This will install the Cryptography package and its dependencies.

#### Using setup.py

1. Check if Python is installed: 
    - Open a command prompt window and type `python --version`. 
    - If Python is not installed, follow the instructions [here](https://www.python.org/downloads/) to install it.

2. Install the Cryptography package: 
    - Download the Cryptography package from [here](https://pypi.org/project/cryptography/). 
    - Extract the downloaded file and open a command prompt window in the extracted folder. 
    - Type `python setup.py install` to install the Cryptography package and its dependencies.
