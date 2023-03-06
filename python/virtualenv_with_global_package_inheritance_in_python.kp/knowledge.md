---
title: Ensure that specific packages from your global site-packages are inherited by your virtualenv
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `--system-site-packages` option when creating the virtual environment to inherit specific packages from the global site-packages.
---

**Contents**

[TOC]

## Introduction
Virtualenv is a tool to create isolated Python environments. It is useful when we want to work on different Python projects with different dependencies without worrying about version clashes. However, sometimes we may want to inherit specific packages from our global site-packages in Python to our virtualenv environment. This tutorial will guide you through the steps to make it possible.

## Step 1: Creating a virtualenv environment
The first step is to create a virtualenv environment using the following command:

```
$ virtualenv myproject
```

This command will create a new directory "myproject" that contains a Python interpreter and other essential packages necessary to run a Python project.


## Step 2: Identifying packages to be inherited
The next step is to identify the specific packages that you would like to inherit from your global site-packages in Python. To do this, you can run the following command:

```
$ pip freeze > requirements.txt
```

This command will create a requirements.txt file in your current directory containing a list of all the packages installed in your global site-packages.


## Step 3: Creating a virtualenv with global site-packages
To create a new virtualenv environment with packages inherited from your global site-packages, you can use the following command:

```
$ virtualenv --system-site-packages myproject
```

This command tells virtualenv to use the packages installed in your global site-packages directory and also includes them in your virtualenv environment. Now, any packages installed globally will also be available in your virtualenv environment.


## Step 4: Activating the virtualenv environment
To activate the virtualenv environment, you can use the following command:

```
$ source myproject/bin/activate
```

This command will activate your virtualenv environment, and you can now install additional packages as needed for your project.

## Conclusion
In conclusion, it is possible to inherit specific packages from your global site-packages in Python to your virtualenv environment. This tutorial has outlined the steps to achieve this, including creating a virtualenv environment, identifying packages to be inherited, creating a virtualenv with global site-packages, and activating the virtualenv environment. By following these steps, you can work on different Python projects with different dependencies without worrying about version clashes.
