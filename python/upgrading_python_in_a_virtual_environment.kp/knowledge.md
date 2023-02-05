---
title: Update the version of Python used in a virtual environment
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To update Python in a virtualenv, use the command `pip install --upgrade pip` in the virtualenv.
---

**Contents**

[TOC]

# Step 1: Create a Virtual Environment

Creating a virtual environment allows you to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them.

To create a virtual environment, you can use the `virtualenv` command. To create a virtual environment called `my_env`, use the following command:

```
virtualenv my_env
```

# Step 2: Activate the Virtual Environment

Once you have created a virtual environment, you need to activate it. To activate the `my_env` environment, use the following command:

```
source my_env/bin/activate
```

# Step 3: Install Python

Once the virtual environment is activated, you can install Python in it. To install Python in the `my_env` environment, use the following command:

```
pip install python
```

# Step 4: Upgrade Python

Once Python is installed in the virtual environment, you can upgrade it. To upgrade Python in the `my_env` environment, use the following command:

```
pip install --upgrade python
```
