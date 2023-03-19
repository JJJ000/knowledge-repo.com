---
title: How to utilize pip for Python versions 3.x while concurrently using Python versions 2.x
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use pip3 instead of pip to ensure packages are installed for Python 3.x alongside Python 2.x.
---

**Contents**

[TOC]

## Introduction

Pip is a package management system used to install and manage software packages written in Python. In this tutorial, we will learn how to use pip with Python 3.x alongside Python 2.x.


## Step 1: Determine pip version

The first step is to determine the version of pip installed for Python 3.x. Run the following command to check the pip version:

```
pip3 --version
```

You should see something like this:

```
pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)
```

## Step 2: Install packages for Python 3.x

To install packages for Python 3.x, use the command `pip3 install`. For example, to install the `requests` package:

```
pip3 install requests
```

This will install the `requests` package for Python 3.x.

## Step 3: Use pip with Python 2.x

To use pip with Python 2.x, use the command `pip`. For example, to install the `numpy` package for Python 2.x:

```
pip install numpy
```

This will install the `numpy` package for Python 2.x.

## Step 4: Verify package installation

To verify that the packages were installed correctly, you can use the command `pip list`. This will list all the installed packages for both Python 2.x and Python 3.x.

```
pip list
```

You should see both the `requests` and `numpy` packages listed in the output, each indicating the version and which Python version it is installed for.

```
Package         Version    Python
--------------- ---------- -------
numpy           1.18.1     2.7
requests        2.25.1     3.8
```
