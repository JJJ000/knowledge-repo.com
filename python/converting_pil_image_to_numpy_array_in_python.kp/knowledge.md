---
title: What is the process for transforming a pil image into a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can convert a PIL Image into a NumPy array by calling the `np.array()` method on the Image object.
---

**Contents**

[TOC]

# Section 1: Import Libraries 

First, you will need to import the necessary libraries. This includes the `PIL` library and the `NumPy` library.

```python
from PIL import Image
import numpy as np
```

# Section 2: Load Image

Next, you will need to load the image you wish to convert into a `PIL` object. 

```python
image = Image.open('image.jpg')
```

# Section 3: Convert to NumPy Array

Now, you can convert the `PIL` object into a NumPy array using the `np.array()` method.

```python
image_array = np.array(image)
```

# Section 4: Print Image Array

Finally, you can print the NumPy array to check the conversion.

```python
print(image_array)
```
