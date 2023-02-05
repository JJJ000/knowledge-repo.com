---
title: What is the procedure for cropping an image in opencv using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the cv2.imshow() and cv2.getRectSubPix() functions to crop an image in OpenCV using Python.
---

**Contents**

[TOC]

## Section 1: Importing Necessary Modules

In order to crop an image using OpenCV and Python, we must first import the necessary modules. This includes the `cv2` module, which provides us with the functions necessary to work with OpenCV.

```python
import cv2
```

## Section 2: Reading the Image

Once the necessary modules have been imported, we must read the image into memory. This can be done using the `cv2.imread()` function, which takes the path to the image as an argument.

```python
img = cv2.imread('path/to/image.jpg')
```

## Section 3: Cropping the Image

Once the image is loaded into memory, we can crop it using the `cv2.rectangle()` function. This function takes four arguments: the image, the top-left corner of the crop, the bottom-right corner of the crop, and the color of the rectangle.

```python
x1, y1 = 0, 0 # Top left corner
x2, y2 = 100, 100 # Bottom right corner

cropped_img = img[y1:y2, x1:x2] # Crop the image
cv2.rectangle(img, (x1, y1), (x2, y2), (0, 255, 0), 2) # Draw a rectangle around the crop
```

## Section 4: Saving the Cropped Image

Finally, we can save the cropped image using the `cv2.imwrite()` function. This function takes two arguments: the path to the output file, and the image to be saved.

```python
cv2.imwrite('path/to/cropped_image.jpg', cropped_img)
```
