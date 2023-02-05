---
title: Show only the files in the current directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: os.listdir(`.`) will return a list of files in the current directory.
---

**Contents**

[TOC]

1. Using `os.listdir` 

```python
import os

files = os.listdir('.')
```

2. Using `os.scandir`

```python
import os

files = [entry.name for entry in os.scandir('.') if entry.is_file()]
```

3. Using `glob`

```python
import glob

files = glob.glob('*')
```

4. Using `pathlib`

```python
from pathlib import Path

files = [file.name for file in Path('.').iterdir() if file.is_file()]
```
