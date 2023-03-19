---
title: What is the process for using the matplotlib colormap to turn a numpy array into a pil image?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To convert a NumPy array to PIL image with a matplotlib colormap in Python, use matplotlib`s `cm` submodule to get the colormap and then create an RGB image using `PIL.Image.fromarray()` and the colormap.
---

**Contents**

[TOC]

## Section 1: Import required libraries
To convert a NumPy array to PIL image and apply matplotlib colormap in Python, we need to import the required libraries. We will use the following libraries:
- `numpy` for handling NumPy arrays.
- `PIL` for converting NumPy arrays to images.
- `matplotlib` for applying colormaps to the NumPy arrays. 

```python
import numpy as np
from PIL import Image
import matplotlib.pyplot as plt
``` 

## Section 2: Create NumPy array and apply colormap
We will create a random NumPy array and apply a colormap using `matplotlib`. We will use `jet` colormap as an example. You can choose any other colormap from `matplotlib.cm` library.

```python
# create random NumPy array
arr = np.random.rand(256, 256)

# apply colormap
cmap = plt.get_cmap('jet')
rgba_img = cmap(arr)
```

## Section 3: Convert to PIL image
We need to convert the `rgba_img` NumPy array to PIL image using `Image.fromarray()` method.

```python
# convert to PIL image
pil_img = Image.fromarray((rgba_img*255).astype(np.uint8))
```

## Section 4: Save or display image
Finally, we can save or display the PIL image using `save()` and `show()` methods respectively.

```python
# save the image
pil_img.save('output.jpg')

# display the image
pil_img.show()
``` 

This way, we can easily convert a NumPy array to PIL image applying matplotlib colormap in Python.
