---
title: The command for virtualenv could not be found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Virtualenv is not a part of the Python standard library and must be installed separately.
---

**Contents**

[TOC]

# Solution

## Installing Virtualenv

Virtualenv is a tool used to create isolated Python environments. It allows you to create independent environments for different projects, where you can install packages without affecting the other environments.

To install Virtualenv, you can use the pip command:

```
pip install virtualenv
```

## Using Virtualenv

Once you have installed Virtualenv, you can create a new environment with the following command:

```
virtualenv my_env
```

This will create a new environment called `my_env` in the current directory. To activate this environment, you can use the following command:

```
source my_env/bin/activate
```

Once the environment is activated, you can install packages in it without affecting the other environments. To deactivate the environment, you can use the `deactivate` command.

## Troubleshooting

If you encounter an error saying `virtualenv: command not found`, then it means that virtualenv is not installed on your system. To install it, you can use the `pip` command as mentioned above.
