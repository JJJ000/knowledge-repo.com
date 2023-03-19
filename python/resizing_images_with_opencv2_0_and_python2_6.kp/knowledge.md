---
title: How to modify the dimensions of an image using opencv2.0 and python2.6
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the cv2.resize() function in OpenCV2.0 and Python2.6 to resize an image.
---

**Contents**

[TOC]

Introduction

OpenCV (Open Source Computer Vision Library) is an open source computer vision and machine learning software library that provides a variety of image processing functions. It includes a large number of image processing algorithms and functions for image manipulation, math operations, and image analysis, and can be used with Python for image processing and computer vision tasks. In this article, we will discuss how to resize an image using OpenCV 2.0 and Python 2.6.

Importing OpenCV Libraries

The first step is to import the necessary OpenCV libraries. OpenCV can be installed using pip, and the libraries can be imported using the following code:

```
import cv2
import numpy as np
```

Here, we have imported the cv2 library and the numpy library for numerical processing.

Loading the Image

Once the libraries have been imported, we can load the image that we want to resize. We can do this using the cv2.imread() function. This function takes the path of the image as a parameter and loads the image in a numpy array. Here’s an example code to load an image:

```
# Load the image
img = cv2.imread('myimage.jpg')
```

Here, we have loaded an image called ‘myimage.jpg’. You can replace this with the path of the image that you want to resize.

Resizing the Image

To resize an image using OpenCV, we can use the cv2.resize() function. This function takes the following parameters:

- img: The input image that we want to resize
- dsize: The desired size of the output image (in pixels)
- fx: The scaling factor in the x-direction
- fy: The scaling factor in the y-direction
- interpolation: The interpolation method to be used. The most common methods are cv2.INTER_LINEAR and cv2.INTER_NEAREST.

Here’s an example code to resize the image to half its size:

```
# Get the original height and width of the image
height, width = img.shape[:2]

# Set the new size of the image
new_width = width // 2
new_height = height // 2

# Resize the image
resized_img = cv2.resize(img, (new_width, new_height))
```

In this code, we first get the original height and width of the image using the img.shape property. Then, we set the new size of the image by dividing the original height and width by 2. Finally, we resize the image using cv2.resize() and store the resized image in a new variable called resized_img.

Displaying the Resized Image

Once the image has been resized, we can display it using the cv2.imshow() function. Here’s an example code to display the resized image:

```
# Display the resized image
cv2.imshow('Resized Image', resized_img)

# Wait for a key to be pressed
cv2.waitKey(0)

# Destroy the window
cv2.destroyAllWindows()
```

In this code, we first call the cv2.imshow() function to display the resized image in a window called ‘Resized Image’. Then, we call the cv2.waitKey() function to wait for a key to be pressed, and the cv2.destroyAllWindows() function to close the window when a key is pressed.

Conclusion

In this article, we discussed how to resize an image using OpenCV 2.0 and Python 2.6. We first imported the necessary OpenCV libraries, loaded the image that we want to resize, resized the image using the cv2.resize() function, and then displayed the resized image using the cv2.imshow() function. By following these steps, you can easily resize any image using OpenCV and Python.
