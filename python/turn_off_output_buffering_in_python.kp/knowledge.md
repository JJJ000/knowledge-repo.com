---
title: Turn off output buffering
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Disable output buffering by setting the `flush` parameter of the print function to True.
---

**Contents**

[TOC]

### 1. Turning Off Output Buffering

Output buffering can be disabled in Python by setting the `PYTHONUNBUFFERED` environment variable to `1`. This can be done by running the following command in the terminal:

```
export PYTHONUNBUFFERED=1
```

Alternatively, this can be done programmatically in Python by setting the `os.environ['PYTHONUNBUFFERED']` environment variable to `1`:

```python
import os
os.environ['PYTHONUNBUFFERED'] = '1'
```

### 2. Disabling Buffering for the Python Interpreter

The Python interpreter can be launched with the `-u` flag to disable output buffering:

```
python -u <script>
```

### 3. Disabling Buffering for the Python Script

The `-u` flag can also be used when running a Python script to disable output buffering:

```
python -u <script>
```

### 4. Disabling Buffering for the sys.stdout Stream

The `sys.stdout` stream can be set to be unbuffered by setting its `.buffer` attribute to `None`:

```python
import sys
sys.stdout.buffer = None
```
