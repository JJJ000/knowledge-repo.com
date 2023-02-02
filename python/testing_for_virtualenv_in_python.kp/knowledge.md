---
title: Check if Python is running in a virtual environment
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can determine if Python is running inside virtualenv by checking if the environment variable VIRTUAL\_ENV is set.
---

**Contents**

[TOC]

# Checking the Environment

One way to determine if Python is running inside virtualenv is to check the environment. The `VIRTUAL_ENV` environment variable will be set if the Python interpreter is running inside a virtualenv.

# Checking the Python Version

Another way to determine if Python is running inside virtualenv is to check the Python version. Virtualenv will modify the Python version string to include the virtualenv name.

# Checking the Path

Yet another way to determine if Python is running inside virtualenv is to check the path. Virtualenv will add the virtualenv's `bin` directory to the beginning of the `PATH` environment variable.
