---
title: What is the process for operating conda?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Type `conda` in the command prompt or terminal followed by any desired Conda command.
---

**Contents**

[TOC]

## Installing Conda

First of all, you need to install **Conda** on your system. 

1. Visit the [official Conda website](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) and download the installer appropriate for your operating system.
2. Follow the instructions to install Conda on your system.

## Activating Conda Environment

After Conda has been installed, you need to activate it before using it in Python.

1. Open a terminal window or Anaconda Prompt (if you are using Windows) and type the command `conda init` to initialize the shell.
2. Close and reopen the terminal window.
3. Type the command `conda activate` to activate the base environment.

## Using Conda in Python

Once Conda has been installed and activated, you can use it in Python in the following way:

1. Open a Python interpreter or create a Python script.
2. Import any package you want to use that is available in your Conda environment. For example, if you want to import the `numpy` package, you can simply type `import numpy`.
3. Conda will automatically use the version of the package that is installed in your active environment.

## Creating a New Conda Environment

You can also create a new Conda environment to install packages in.

1. Open a terminal window or Anaconda Prompt and type the command `conda create --name myenv` where `myenv` can be any name you choose for your environment.
2. Activate the new environment by typing the command `conda activate myenv`.
3. Install any packages you want to use in this environment using the command `conda install <package_name>`. For example, to install the `numpy` package, you can type `conda install numpy`.
