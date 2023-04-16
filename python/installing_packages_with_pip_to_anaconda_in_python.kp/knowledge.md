---
title: Installing packages to anaconda environment with pip
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To install packages to an Anaconda environment in Python, use the `conda install` command in the Anaconda Prompt.
---

**Contents**

[TOC]

## Installation

To install packages to an Anaconda environment using pip, you must first activate the Anaconda environment. To do this, open the Anaconda prompt and type the following command:

`conda activate <environment_name>`

For example, if your environment is called "my_env", you would type:

`conda activate my_env`

## Installing Packages

Once the environment is activated, you can install packages using pip. To install a package, type the following command:

`pip install <package_name>`

For example, to install the "requests" package, you would type:

`pip install requests`

## Updating Packages

If you already have a package installed and want to update it to the latest version, you can use the following command:

`pip install --upgrade <package_name>`

For example, to update the "requests" package, you would type:

`pip install --upgrade requests`

## Uninstalling Packages

If you want to uninstall a package, you can use the following command:

`pip uninstall <package_name>`

For example, to uninstall the "requests" package, you would type:

`pip uninstall requests`
