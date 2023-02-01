---
title: What is the procedure for changing the name of a conda environment?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can rename a conda environment in Python by using the `conda env rename` command.
---

**Contents**

[TOC]

## 1. Using the Command Line

Using the command line, you can rename a conda environment by using the `conda env` command. The syntax for this command is `conda env rename <old_name> <new_name>`. This will rename the specified environment from `<old_name>` to `<new_name>`.

## 2. Using Anaconda Navigator

You can also rename a conda environment using the Anaconda Navigator graphical user interface. To do this, open the Anaconda Navigator and click on the Environments tab. Select the environment you wish to rename, then click the gear icon next to it. This will open a window where you can enter the new name for the environment. Once you have entered the new name, click the "Rename" button to save the new name.

## 3. Using Conda API

You can also rename a conda environment using the Conda API. To do this, you need to first import the `conda.cli.python.rename_env` function. Then, you can call this function with the old and new environment names as arguments. This will rename the specified environment from `<old_name>` to `<new_name>`.

## 4. Using Python

Finally, you can also rename a conda environment using Python. To do this, you need to first import the `conda.cli.python.rename_env` function. Then, you can call this function with the old and new environment names as arguments. This will rename the specified environment from `<old_name>` to `<new_name>`.
