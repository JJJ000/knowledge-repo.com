---
title: Converting a numpy array into an image file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the numpy.save() or numpy.savez() functions to save a Numpy array as an image.
---

**Contents**

[TOC]

### Using PIL Library

The Python Imaging Library (PIL) provides support for many image formats. To save a numpy array as an image we can use the `Image.fromarray()` function.

```python
from PIL import Image
import numpy as np

# Create a numpy array
arr = np.random.randint(0, 255, size=(100, 100, 3), dtype=np.uint8)

# Create an Image object from the array
img = Image.fromarray(arr)

# Save the image
img.save('my_image.png')
```

### Using Matplotlib

Matplotlib is a plotting library for Python. It provides functions to save plots as images. To save a numpy array as an image we can use the `plt.imsave()` function.

```python
import matplotlib.pyplot as plt
import numpy as np

# Create a numpy array
arr = np.random.randint(0, 255, size=(100, 100, 3), dtype=np.uint8)

# Save the array as an image
plt.imsave('my_image.png', arr)
```
