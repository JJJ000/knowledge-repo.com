---
title: What is the process to activate a virtualenv using pycharm's terminal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To activate a virtualenv inside PyCharm`s terminal in Python, simply run the command `source path/to/venv/bin/activate` in the terminal.
---

**Contents**

[TOC]

# Creating a virtual environment in PyCharm

The first step is to create a virtual environment in PyCharm. This can be done by following these steps:

1. Open your PyCharm project and navigate to the project interpreter settings by clicking on the File menu and selecting Settings.
2. In the Settings dialog box, click on the Project: <your project name> option and then select the Python Interpreter option from the left-hand menu.
3. Click on the gear icon next to the Project Interpreter drop-down menu and select the Add option. 

# Activating the virtual environment

Once you have created your virtual environment, you can activate it in PyCharm's terminal by following these steps:

1. Open the PyCharm terminal by clicking on the Terminal tab at the bottom of the PyCharm window.
2. Navigate to the project directory in the terminal using the cd command.
3. Once you are in the project directory, activate the virtual environment by running the following command: source <path to virtual environment>/bin/activate.
4. After running the activate command, you should see the name of the virtual environment appear in parentheses at the beginning of the terminal prompt. This indicates that you have successfully activated the virtual environment.

# Installing packages in the virtual environment

With the virtual environment activated, you can now install packages using pip. To install a package, simply run the following command:

`pip install <package name>`

This will install the package in the virtual environment, rather than globally on your system. You can confirm that the package has been installed by running the `pip freeze` command, which will list all of the packages installed in the virtual environment.

# Deactivating the virtual environment

When you are finished working in the virtual environment, you can deactivate it by running the following command:

`deactivate`

This will return you to your system's default Python environment. You can confirm that the virtual environment has been deactivated by checking that the virtual environment name no longer appears in parentheses at the beginning of the terminal prompt.
