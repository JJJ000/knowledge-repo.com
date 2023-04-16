---
title: What is the most efficient way to determine the current cpu and ram usage using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The psutil library can be used to get the current CPU and RAM usage in Python.
---

**Contents**

[TOC]

## Using psutil

The [psutil](https://pypi.org/project/psutil/) library is a great tool for retrieving system information such as CPU and RAM usage.

### Installation

To install psutil, simply run the following command in your terminal:

`pip install psutil`

### Usage

Once psutil is installed, you can easily get the current CPU and RAM usage by using the following code:

```python
import psutil

cpu_usage = psutil.cpu_percent()
ram_usage = psutil.virtual_memory().percent

print(f'CPU Usage: {cpu_usage}%')
print(f'RAM Usage: {ram_usage}%')
```

This will print out the current CPU and RAM usage in percentage.
