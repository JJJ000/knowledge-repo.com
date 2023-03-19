---
title: The error message "importerror no module named bs4 (beautifulsoup)" could be rephrased as, "there is an issue with importing the module named bs4 (beautifulsoup) as it cannot be found."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You need to install BeautifulSoup module by running `pip install beautifulsoup4` in command prompt/terminal.
---

**Contents**

[TOC]

# Overview
When the "No Module Named bs4 (BeautifulSoup)" error is encountered in Python, it typically means that the BeautifulSoup library is missing or has not been properly installed in the local system. 

This error can be frustrating and confusing, especially for beginners. However, with some basic troubleshooting steps, this issue can be resolved effectively.


# Check if BeautifulSoup is Installed
Before we can start using BeautifulSoup, we need to ensure that it is properly installed in our system. One way to do this is by checking if the package is listed in the installed packages list.

This can be done by typing the following command in the terminal:

```
pip list
```

This command displays all the Python packages that are installed on the system. If BeautifulSoup is not listed in the output, then it means that the library is not installed.

In this case, we need to install the package using the following command:

```
pip install beautifulsoup4
```

# Check if Installation is Complete
After installing BeautifulSoup using the above command, it's a good idea to verify if the installation is complete by importing the package in our Python code.

This can be done by opening a Python shell and typing:

```python
from bs4 import BeautifulSoup
```

If no errors are raised, then it means that BeautifulSoup has been installed successfully and is ready to be used.

# Conclusion
In this tutorial, we learned how to resolve the "No Module Named bs4 (BeautifulSoup)" error in Python. This can be done by checking if BeautifulSoup is installed, installing it if needed and verifying the installation by importing it in our Python code. Following these steps should help fix the issue and allow the user to make use of the BeautifulSoup package within their Python code.
