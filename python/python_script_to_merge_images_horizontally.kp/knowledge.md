---
title: Create a horizontal arrangement of multiple images using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the concatenate function from the OpenCV library to combine multiple images horizontally in Python.
---

**Contents**

[TOC]

# Introduction
Combining images horizontally is a common task in computer vision and image processing. In this tutorial, we will learn how to combine several images horizontally using Python.

# Required Packages
To achieve this task, we will use the following packages:
- `numpy`: for numerical operations on images.
- `cv2`: OpenCV library for reading and writing images.

# Loading Images
To combine images horizontally, we need to load them first. In this example, we will load four images named `image1.jpg`, `image2.jpg`, `image3.jpg`, and `image4.jpg`.

```python
import cv2
import numpy as np

# Load images
image1 = cv2.imread('image1.jpg')
image2 = cv2.imread('image2.jpg')
image3 = cv2.imread('image3.jpg')
image4 = cv2.imread('image4.jpg')
```

# Combining Images Horizontally Using Numpy
Now that we have loaded the images, we can combine them horizontally using the `numpy` library. We can use the `hstack` function in `numpy` to stack the images horizontally.

```python
# Combine images horizontally using numpy
combined_image = np.hstack((image1, image2, image3, image4))

# Save the combined image
cv2.imwrite('combined_image.jpg', combined_image)
```

Here, we have used the `hstack` function to concatenate the input arrays (images) along the horizontal axis. The `combined_image` variable now contains the horizontally stacked images, and we can save it using the `cv2.imwrite` function.

# Combining Images Horizontally Using OpenCV
Alternatively, we can also use the `cv2.hconcat` function in OpenCV to combine images horizontally. Here's how we can use this function:

```python
# Combine images horizontally using OpenCV
combined_image = cv2.hconcat([image1, image2, image3, image4])

# Save the combined image
cv2.imwrite('combined_image.jpg', combined_image)
```

`cv2.hconcat` takes a list of input images as an argument and combines them horizontally. The `combined_image` variable now contains the horizontally stacked images, and we can save it using the `cv2.imwrite` function.

# Conclusion
In this tutorial, we have learned how to combine several images horizontally using Python. We have seen how we can use either the `numpy` library or the `cv2.hconcat` function in OpenCV to achieve this task.
