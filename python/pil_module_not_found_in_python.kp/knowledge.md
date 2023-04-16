---
title: The module named pil could not be imported due to an importerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Python Imaging Library (PIL) must be installed to use PIL in Python.
---

**Contents**

[TOC]

# Solution

## Install Pillow
Pillow is the friendly PIL fork by Alex Clark and Contributors. PIL is the Python Imaging Library by Fredrik Lundh and Contributors.

To install Pillow on Windows machines, download the appropriate wheel file from [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pillow) and install it by running this command in the command prompt:

```
pip install Pillow‑4.2.1‑cp27‑cp27m‑win32.whl
```

## Install PIL
If you still need to use the original PIL, you can install it using pip:

```
pip install PIL
```

## Import PIL
Once you have installed PIL, you can import it in your Python program:

```
from PIL import Image
```

## Troubleshooting
If you encounter any problems when trying to install or import PIL, make sure you are using the correct version of Python and that you have the necessary dependencies installed. You can find more information on the official PIL website [here](https://pillow.readthedocs.io/en/stable/installation.html).
