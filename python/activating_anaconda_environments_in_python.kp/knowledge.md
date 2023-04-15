---
title: What are the steps to activate an anaconda environment?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To activate an Anaconda environment in Python, run the command `conda activate <env\_name>` where env\_name is the name of the environment you want to activate.
---

**Contents**

[TOC]

# Introduction
Anaconda is an open-source distribution platform for Python and R languages. Anaconda not only saves time by providing pre-built packages and tools but it also helps to manage environments in which different Python versions and packages can exist. The Anaconda environments allow working with different projects and isolating package versions that may conflict with each other.

# Viewing Environment List
Before activating an Anaconda environment, it is necessary to know the available environments in Anaconda. To view the list of available environments in the Anaconda, one can run `conda env list` command in the command prompt. 

# Activating an Environment
After listing the available environments in Anaconda, to activate an environment of interest, we need to run the following command in the command prompt: `conda activate <environment name>`. This command will activate the environment with the specified name. Once the environment is activated, the command prompt will reflect the current environment name.

# Deactivating an Environment
When finished working in the activated environment, we can deactivate it using the following command: `conda deactivate`. The environment will be deactivated and the command prompt will return to the default environment. 

These are the basic steps to activate and deactivate an Anaconda environment. These environments are useful when the development workflow requires different versions of packages or Python in different projects, or when testing new packages that should not interfere with others.
