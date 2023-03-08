---
title: Resizing or rescaling images with numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To resize/rescale an image using Numpy in Python, use the cv2.resize() function.
---

**Contents**

[TOC]

## Introduction
In this article, we will discuss how to resize and rescale images using the NumPy library in Python. Image resizing refers to changing the dimensions of an image, while image rescaling refers to changing the size of an image while keeping its dimensions the same. We will cover both these techniques using NumPy in the following sections.

## Resizing Image

Resizing an image involves changing its dimensions. Numpy provides the `resize()` function for this purpose. 

```python
import numpy as np
from PIL import Image

# loading the image
img = Image.open("input_image.jpg")

# converting image to numpy array
img_array = np.array(img)

# resizing the image
new_img = np.resize(img_array, (new_height, new_width))

# saving the resized image
resized_img = Image.fromarray(new_img)
resized_img.save("resized_image.jpg")
```

Here, we first load the image using the `PIL` library, and then convert it into a numpy array using the `np.array()` method. We then use the `np.resize()` method to resize the image to the desired dimensions. Finally, we create an instance of the `Image` class and save the resized image.

## Rescaling Image

Rescaling an image involves changing its size while keeping its dimensions the same. Numpy provides the `interploate()` method for this purpose. 

```python
import numpy as np
from PIL import Image

# loading the image
img = Image.open("input_image.jpg")

# converting image to numpy array
img_array = np.array(img)

# specifying the scaling factor
scale = 0.5

# calculating the new height and width
new_height = int(img_array.shape[0] * scale)
new_width = int(img_array.shape[1] * scale)

# rescaling the image
new_img = np.zeros((new_height, new_width, img_array.shape[2]), dtype=np.uint8)

for channel in range(img_array.shape[2]):
    for i in range(new_height):
        for j in range(new_width):
            x = int(i/scale)
            y = int(j/scale)
            new_img[i,j,channel] = img_array[x,y,channel]

# saving the rescaled image
rescaled_img = Image.fromarray(new_img)
rescaled_img.save("rescaled_image.jpg")

```

Here, we first load the image using the `PIL` library, and then convert it into a numpy array using the `np.array()` method. We then specify the scaling factor and calculate the new height and width of the image. We then create a new image with the new dimensions and loop through each channel of the image. We then loop through each pixel of the new image and interpolate the values from the original image. Finally, we create an instance of the `Image` class and save the rescaled image.

## Conclusion

In this article, we discussed how to resize and rescale images using the NumPy library in Python. We covered both these techniques and provided examples for each. These techniques can be applied to images of any dimensions and resolution.
