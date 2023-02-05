---
title: Obtain a list of files in a directory that have been processed through a filter
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the os.listdir() function with a filter argument to get a filtered list of files in a directory in Python.
---

**Contents**

[TOC]

**Section 1: Importing Libraries**

```python
from os import listdir
from os.path import isfile, join
```

**Section 2: Defining the Filter**

```python
filter_extension = ".txt"
```

**Section 3: Getting the Files**

```python
mypath = 'C:/MyDirectory/'
files = [f for f in listdir(mypath) if isfile(join(mypath, f))]
```

**Section 4: Filtering the Files**

```python
filtered_files = [f for f in files if f.endswith(filter_extension)]
```
