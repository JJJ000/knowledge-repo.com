---
title: The difference between os.getenv and os.environ.get is that os.getenv will return the value of an environment variable for a given key, while os.environ.get will return the entire environment dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: os.getenv() gets the value of the environment variable with the specified name, while os.environ.get() gets the value of the environment variable, or a default value if the variable is not set.
---

**Contents**

[TOC]

# os.getenv

os.getenv() is a function in the os module that retrieves the value of an environment variable. It takes a single argument, the name of the environment variable, and returns the value of the variable as a string.

# os.environ.get

os.environ.get() is a method in the os module that retrieves the value of an environment variable. It takes two arguments, the name of the environment variable and a default value to return if the variable does not exist. It returns the value of the variable as a string or the default value if the variable does not exist.

# Difference

The main difference between os.getenv and os.environ.get is that os.getenv will throw an error if the environment variable does not exist, while os.environ.get will return a default value if the environment variable does not exist.
