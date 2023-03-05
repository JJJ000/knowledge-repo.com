---
title: What is the process of converting an rgb image to grayscale using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the convert() method from the Pillow library to convert the image into grayscale.
---

**Contents**

[TOC]

## Importing libraries

The first step is to import the necessary libraries - NumPy and OpenCV. NumPy is used to deal with arrays, while OpenCV is used for image processing.

```python
import numpy as np
import cv2
```

## Loading the image

The next step is to load the image in RGB format using OpenCV's imread() function. The image is stored as a NumPy array.

```python
img = cv2.imread('image.jpg')
```

## Converting to grayscale

We can convert the RGB image to grayscale using OpenCV's cvtColor() function. The function takes two arguments - the input image and the color space conversion code. To convert an RGB image to grayscale, we need to pass the code cv2.COLOR_RGB2GRAY as the second argument.

```python
gray_img = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)
```

## Displaying the result

To display the grayscale image, we can use the imshow() function of OpenCV. It takes two arguments - the title of the window and the image to be displayed.

```python
cv2.imshow('Grayscale Image', gray_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

The above code will display the grayscale image in a new window titled 'Grayscale Image'. The waitKey() function allows us to display the image until a key is pressed, after which the window is destroyed using the destroyAllWindows() function.
