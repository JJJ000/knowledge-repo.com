---
title: After installing pip, where can virtualenvwrapper.sh be found?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The virtualenvwrapper.sh file is usually located in the bin folder within the virtual environment created by virtualenvwrapper.
---

**Contents**

[TOC]

## Introduction
`virtualenvwrapper` is a tool that is used to manage multiple virtual environments in Python. To organize all virtual environments in one place, we can use `virtualenvwrapper.sh`. This file is created when you install `virtualenvwrapper` using pip. 

## Check virtualenvwrapper installation
Before we locate `virtualenvwrapper.sh`, we need to check whether `virtualenvwrapper` is installed on your system or not. To do this, open the Python console and type the following command:

```python
import virtualenvwrapper
```

If the module is not installed on the system, you will get an error message: `ModuleNotFoundError: No module named 'virtualenvwrapper'`. In this case, you should run the following command:

```python
!pip install virtualenvwrapper
```

## Locate virtualenvwrapper.sh
`virtualenvwrapper.sh` is usually installed in the `/usr/local/bin/` directory or `~/.local/bin/` directory. To locate the file, go to the terminal and run the following command:

```console
which virtualenvwrapper.sh
```

This will output a path that leads to `virtualenvwrapper.sh`. 

## Add virtualenvwrapper.sh to the shell
In order to use `virtualenvwrapper`, you need to add `virtualenvwrapper.sh` to the shell. If the file is located in `/usr/local/bin/` directory, add the following command to your `.bashrc` or `.bash_profile` file:

```console
source /usr/local/bin/virtualenvwrapper.sh
```

If the file is located in the `~/.local/bin/` directory, add the following command to your `.bashrc` or `.bash_profile` file:

```console
source ~/.local/bin/virtualenvwrapper.sh
```

After adding this command, restart your terminal for the changes to take effect. 

Now, you can use `virtualenvwrapper` to create and manage virtual environments in Python.
