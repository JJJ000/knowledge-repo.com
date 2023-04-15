---
title: The module 'crypto.cipher' cannot be found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Cryptography module (formerly Crypto) is not imported or installed in Python.
---

**Contents**

[TOC]

Section 1: Introduction
If you have encountered the error "ImportError: No module named Crypto.Cipher" in Python, it means that the module "Crypto.Cipher" is not installed on your system or can't be found by Python.

In this guide, we'll go through the different reasons why this error might occur and how to fix it.

Section 2: Check if the module is installed
The first thing to check is if the "pycryptodome" module, which contains "Crypto.Cipher," is installed on your system. You can do this by opening your command prompt or terminal and typing:

```
pip list
```
This will give you a list of all the Python packages installed on your system. Look for "pycryptodome" in the list. If it's not there, you need to install it by typing:

```
pip install pycryptodome
```

Section 3: Check if the module is imported correctly
Make sure that the "Crypto.Cipher" module is imported correctly in your Python code. The correct way to import it is as follows:

```
from Crypto.Cipher import AES
```

If you are still getting the error, try importing the "Crypto" module first and then the "Cipher" module like this:

```
from Crypto import Cipher
```

Also, make sure that you're not using any aliases for the module or its functions, as this can cause the "ImportError" exception to be raised.

Section 4: Conclusion
In conclusion, the "ImportError: No module named Crypto.Cipher" error in Python can be caused by a missing or incorrectly installed "pycryptodome" module or an incorrect import method. Make sure to check that the module is installed correctly and that it's being imported correctly in your code.
