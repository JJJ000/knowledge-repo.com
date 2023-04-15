---
title: What is the method for determining the version of pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Type `pip --version` in the command prompt to know the version of pip itself in Python.
---

**Contents**

[TOC]

## Section 1: Finding the location of the pip executable

Before checking the version of pip, we need to know the location of the pip executable file.

We can find the location of the pip executable by running the following command in the terminal:

```bash
which pip
```

This command will output the path of the pip executable. The output may look like this:

```
/usr/local/bin/pip
```

## Section 2: Checking the version of pip using pip command

Once we have the location of the pip executable, we can check the version of pip using the following command:

```bash
pip --version
```

This command will output the version of pip installed on your system. The output may look like this:

```
pip 20.2.3 from /usr/local/lib/python3.8/site-packages/pip (python 3.8)
```

## Section 3: Checking the version of pip using python command

Alternatively, we can also check the version of pip using the following python command:

```python
import pip
print(pip.__version__)
```

This command will output the version of pip installed on your system. The output may look like this:

```
20.2.3
```

## Section 4: Upgrading pip to the latest version

If you have an older version of pip installed on your system and you want to upgrade it to the latest version, you can use the following command:

```bash
pip install --upgrade pip
```

This command will upgrade pip to the latest version available.
