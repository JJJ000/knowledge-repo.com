---
title: What is the version of pandas that is installed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The installed pandas version can be found by running the command `pandas.\_\_version\_\_` in Python.
---

**Contents**

[TOC]

# Section 1: Check Version Using the Pandas Module

The easiest way to find the version of pandas that is installed is to use the `__version__` attribute of the pandas module.

```python
import pandas as pd

pd.__version__
```

# Section 2: Check Version Using the Pip Package Manager

If you have installed pandas using the pip package manager, you can check the version of pandas by running the following command in the terminal:

```
pip show pandas
```

# Section 3: Check Version Using the Anaconda Package Manager

If you have installed pandas using the Anaconda package manager, you can check the version of pandas by running the following command in the terminal:

```
conda list pandas
```

# Section 4: Check Version Using the Conda Package Manager

If you have installed pandas using the conda package manager, you can check the version of pandas by running the following command in the terminal:

```
conda list pandas
```
