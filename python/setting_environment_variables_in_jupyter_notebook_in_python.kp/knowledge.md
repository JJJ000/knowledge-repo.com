---
title: What is the process of configuring environment variables in jupyter notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the following syntax to set an environment variable in Jupyter notebook %env VARIABLE\_NAME=value.
---

**Contents**

[TOC]

#### 1. Introduction
In this tutorial, we will learn how to set environment variables in Jupyter notebook using Python. Environmental variables are used to store specific values or configurations to be used by the operating system or applications.


#### 2. Setting Environment Variables in Jupyter Notebook

To set environment variables in Jupyter notebook, we will use the `os` module in Python. Here's an example of setting a new environment variable:


```python
import os

os.environ['ENV_VARIABLE'] = 'value'
```


#### 3. Checking if Environment Variable is set
 After setting the environment variable, it's important to confirm if it was set correctly. To check if the environment variable was set correctly, we can use the `os.getenv()` function. Here's an example:

```python
import os

os.environ['ENV_VARIABLE'] = 'value'

print(os.getenv('ENV_VARIABLE'))
```
The output should be 'value' if the environment variable was set correctly.


#### 4. Conclusion
Setting environment variables in Jupyter notebook is quite essential to ensure smooth functioning. With Python's in-built "os" module, users can easily set environment variables and get their value by providing the correct key. Whether it's for databases, API keys or any other purpose, setting environment variables can make development a lot easier. I hope this guide has been useful to you.
