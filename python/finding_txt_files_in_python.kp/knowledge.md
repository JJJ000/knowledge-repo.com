---
title: Search for all .txt files in a directory using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the glob module to find all files in a directory with a `.txt` extension glob.glob(`directory/*.txt`)
---

**Contents**

[TOC]

### Using os.listdir

```python
import os

txt_files = [f for f in os.listdir('.') if f.endswith('.txt')]
```

### Using glob

```python
import glob

txt_files = glob.glob('*.txt')
```

### Using Pathlib

```python
from pathlib import Path

txt_files = [f for f in Path('.').glob('*.txt')]
```

### Using os.walk

```python
import os

txt_files = []
for root, dirs, files in os.walk('.'):
    for file in files:
        if file.endswith('.txt'):
            txt_files.append(os.path.join(root, file))
```
