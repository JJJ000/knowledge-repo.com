---
title: What is the syntax for determining the number of cpus using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The number of CPUs can be determined using the Python `os` module, specifically the `os.cpu\_count()` function.
---

**Contents**

[TOC]

### Using the `os` Module

The `os` module allows us to access system information such as the number of CPUs. To find out the number of CPUs using the `os` module, we can use the `os.cpu_count()` function. This function returns the number of CPUs as an integer.

Example:
```python
import os
num_cpus = os.cpu_count()
print(num_cpus) # Outputs 4
```

### Using the `multiprocessing` Module

The `multiprocessing` module also provides a way to find out the number of CPUs. We can use the `multiprocessing.cpu_count()` function to get the number of CPUs. This function also returns the number of CPUs as an integer.

Example:
```python
import multiprocessing
num_cpus = multiprocessing.cpu_count()
print(num_cpus) # Outputs 4
```

### Using the `psutil` Module

The `psutil` module provides a way to get system information such as the number of CPUs. We can use the `psutil.cpu_count()` function to get the number of CPUs. This function also returns the number of CPUs as an integer.

Example:
```python
import psutil
num_cpus = psutil.cpu_count()
print(num_cpus) # Outputs 4
```

### Using the `subprocess` Module

The `subprocess` module provides a way to execute shell commands from within Python. We can use the `subprocess.check_output()` function to execute the `nproc` command, which will return the number of CPUs. This command returns the number of CPUs as a string, so we will need to convert it to an integer.

Example:
```python
import subprocess
num_cpus = int(subprocess.check_output(['nproc']))
print(num_cpus) # Outputs 4
```
