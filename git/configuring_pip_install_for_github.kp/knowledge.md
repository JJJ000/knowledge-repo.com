---
title: Setting up pip to install packages from github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To configure pip install to work from GitHub, add the GitHub repository URL to the pip install command.
---

**Contents**

[TOC]

#### Step 1: Create a setup.py File

In order to install a package from GitHub, you will need to create a setup.py file in the root of your repository. This file is used to define the metadata for your package, such as its name, version, and dependencies.

#### Step 2: Install with pip

Once you have created a setup.py file, you can use pip to install your package directly from GitHub. To do this, you need to use the following command:

`pip install git+https://github.com/<username>/<repo>.git`

Replace <username> and <repo> with your GitHub username and the name of your repository, respectively.

#### Step 3: Test the Installation

Once you have installed your package, you can use the Python interpreter to test that the installation was successful. To do this, you need to import the package and use its functions.

#### Step 4: Publish to PyPI

If you want to make your package available to a wider audience, you can publish it to the Python Package Index (PyPI). This will allow users to install your package using the standard pip install command. To do this, you need to create an account on PyPI and upload your package using the twine tool.
