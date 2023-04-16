---
title: Generate requirements.txt automatically
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use pip freeze to automatically create a requirements.txt file in Python.
---

**Contents**

[TOC]

# Using pip

The `pip` command can be used to generate a `requirements.txt` file. To do so, run the command `pip freeze > requirements.txt` in the terminal. This will create a `requirements.txt` file in the current directory, which will contain all currently installed packages and their versions. 

# Using pipreqs

Another option is to use the `pipreqs` library. This library can be installed using `pip install pipreqs` and then used to generate a `requirements.txt` file. To do so, run the command `pipreqs /path/to/project` in the terminal. This will create a `requirements.txt` file in the specified directory, which will contain all currently installed packages and their versions.

# Using pip-tools

The `pip-tools` library can also be used to generate a `requirements.txt` file. To do so, first install the library using `pip install pip-tools` and then run the command `pip-compile --output-file requirements.txt` in the terminal. This will create a `requirements.txt` file in the current directory, which will contain all currently installed packages and their versions.

# Using setup.py

Finally, you can also use the `setup.py` file to generate a `requirements.txt` file. To do so, add the line `install_requires=[]` to the `setup()` function in the `setup.py` file. Then, run the command `python setup.py install` in the terminal. This will create a `requirements.txt` file in the current directory, which will contain all currently installed packages and their versions.
