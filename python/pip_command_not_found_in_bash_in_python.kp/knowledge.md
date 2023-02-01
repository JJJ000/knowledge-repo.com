---
title: The command 'pip' could not be found in the bash shell
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The pip command is not a built-in command in Python, so it must be installed separately.
---

**Contents**

[TOC]

# Solution

## Step 1: Install Pip

Before you can use `pip`, you need to install it. This can be done with a simple command: 

```
python -m ensurepip --default-pip
```

## Step 2: Update Path

Once `pip` is installed, you need to add it to your system's `PATH` variable. This will allow you to access `pip` from any directory on your system. 

To do this, you will need to open your system's environment variables and add the path to the `pip` executable. 

## Step 3: Use Pip

Once `pip` is installed and your `PATH` is updated, you can use `pip` by simply typing `pip` followed by the command you want to execute. 

For example, if you want to install a package, you can use `pip install <package_name>`.

## Step 4: Troubleshooting

If you are still having issues, you may need to reinstall `pip`. This can be done by running the command `python -m ensurepip --upgrade`.
