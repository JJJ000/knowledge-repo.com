---
title: Ensuring the proper encoding is used when outputting to stdout in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the encoding parameter of the print() function to set the desired encoding.
---

**Contents**

[TOC]

1. Setting the Encoding
----------------------------
The encoding of the output can be set using the `encoding` argument of the `sys.stdout` object.

```python
import sys
sys.stdout = open(sys.stdout.fileno(), mode='w', encoding='utf8')
```

2. Setting the Pipes
------------------------
The encoding can also be set when piping the output of a Python program.

For example, the following command will set the encoding to `utf8` when piping the output of the `my_program.py` file:

```bash
python my_program.py | iconv -f utf8
```

3. Using the `PYTHONIOENCODING` Environment Variable
---------------------------------------------------------
The encoding can also be set using the `PYTHONIOENCODING` environment variable.

For example, the following command will set the encoding to `utf8` when running the `my_program.py` file:

```bash
PYTHONIOENCODING=utf8 python my_program.py
```

4. Using the `python-dotenv` Library
---------------------------------------
The encoding can also be set using the `python-dotenv` library.

For example, the following code will set the encoding to `utf8` when running the `my_program.py` file:

```python
import os
from dotenv import load_dotenv

load_dotenv()
os.environ['PYTHONIOENCODING'] = 'utf8'
```
