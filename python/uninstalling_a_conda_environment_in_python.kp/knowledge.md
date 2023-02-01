---
title: Uninstalling conda environment
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To remove a Conda environment, use the command `conda remove --name <env> --all`.
---

**Contents**

[TOC]

# Section 1: Overview

Conda is an open-source package and environment management system for Python. It is used for managing packages and environments for different versions of Python, as well as for managing packages for different operating systems. It is also used for creating, exporting, and sharing environments.

# Section 2: Removing an Environment

Removing an environment in Conda is a simple process. To remove an environment, first open the Anaconda Prompt and type in the following command: 

`conda env remove -n <environment_name>`

where <environment_name> is the name of the environment you wish to remove. You will then be prompted to confirm the removal.

# Section 3: Deleting Dependencies

Once you have removed the environment, you will need to delete any dependencies that were installed with the environment. To do this, you can use the `conda remove` command. For example, if you want to remove the package `numpy`, you can type the following command:

`conda remove numpy`

# Section 4: Cleaning Up

Finally, you will need to clean up any files that were created when the environment was installed. To do this, you can use the `conda clean` command. This will remove any temporary files and caches that were created when the environment was installed.
