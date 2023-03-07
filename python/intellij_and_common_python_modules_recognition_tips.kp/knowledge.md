---
title: What is the process to make common Python modules recognizable to intellij?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Install the Python plugin and configure the Python interpreter in IntelliJ.
---

**Contents**

[TOC]

## Installing Python Plugin

The first step to getting IntelliJ to recognize common Python modules is to install the Python plugin. To do this, open IntelliJ and go to `File` -> `Settings` -> `Plugins`. In the `Marketplace` tab, search for `Python` and click `Install`. Once the installation is complete, restart IntelliJ.


## Configuring the Project Interpreter

After installing the Python plugin, the next step is to configure the project interpreter. To do this, open the project in IntelliJ and go to `File` -> `Project Structure`. Under `Platform Settings`, select `SDKs`. Click the `+` button to add a new SDK and select `Python SDK`. Choose the appropriate version of Python and click `OK`. 

Then, go to `File` -> `Project Structure` -> `Project Settings` -> `Project` and select the newly added Python SDK as the `Project SDK`.


## Installing Common Python Modules

Once the Python plugin and project interpreter are set up, the final step is to install the common Python modules. To do this, open the Terminal in IntelliJ by going to `View` -> `Tool Windows` -> `Terminal`. Then, use the pip command to install the desired module(s). For example, to install NumPy, type `pip install numpy` and press enter. 

After installing the module(s), close and reopen the project in IntelliJ to ensure the changes are recognized by the IDE. The common Python modules should now be recognized and can be imported in the project code.
