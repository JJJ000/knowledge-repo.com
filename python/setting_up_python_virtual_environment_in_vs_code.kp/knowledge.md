---
title: What is the process of creating a virtual environment for Python in visual studio code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Install the Python extension, create a folder, open it in VS Code, open a new terminal, and type `python3 -m venv env` to create a virtual environment named `env`.
---

**Contents**

[TOC]

## Prerequisites
To set up a virtual environment for Python in Visual Studio Code, you will need the following:
- Visual Studio Code installed on your system
- Python 3 installed on your system

## Create a Virtual Environment
Follow these steps to create a virtual environment in Visual Studio Code:
1. Open Visual Studio Code
2. Open the Terminal by clicking on `Terminal` in the menu bar and selecting `New Terminal`
3. In the terminal, run the following command: `python3 -m venv env`. This will create a new virtual environment in a folder named `env`
4. To activate the environment, run the following command: `source env/bin/activate`. You should now see `(env)` in your terminal prompt, indicating that you are in the virtual environment.
 
## Configure the Interpreter
Follow these steps to configure the interpreter in Visual Studio Code:
1. Press `Ctrl + Shift + P` (or `Cmd + Shift + P` on Mac) to open the Command Palette
2. Search for `Python: Select Interpreter` and press `Enter`
3. Select the interpreter located in the virtual environment you just created (it should be located in the `env/bin` directory)
4. Visual Studio Code will now use this interpreter for Python in the current workspace. You should see the name of the virtual environment displayed in the status bar at the bottom of the screen.

## Deactivate the Virtual Environment
When you are finished working in the virtual environment, you can deactivate it by running the following command: `deactivate`. This will return you to your system's default Python interpreter.
