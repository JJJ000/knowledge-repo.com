---
title: How to eliminate blank spaces surrounding an image that has been saved?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the crop function in the Pillow library to remove white space around a saved image in Python.
---

**Contents**

[TOC]

## Introduction
When saving an image using Python, it is common to encounter white space around the image. This white space is usually caused by the size of the image not matching the size of the underlying canvas. This tutorial will outline methods for removing the unwanted white space from your saved image in Python.

## Option 1: Cropping the Image
One way to remove the white border around a saved image is to crop it. To crop an image in Python, you can use the `crop()` method from the Pillow library. Here's some example code:

```python
from PIL import Image

# Load the image
img = Image.open('image.jpg')

# Get the width and height of the image
width, height = img.size

# Crop the image
img = img.crop((1, 1, width-1, height-1))

# Save the image
img.save('image_cropped.jpg')
```

The `crop()` method takes a tuple of four integers as its argument, which represent the left, upper, right, and lower boundaries of the image to be cropped. In this case, we're cropping one pixel off each side of the image to remove the white space.

## Option 2: Resizing the Canvas
Another way to remove the white border around an image is to resize the canvas to match the size of the image. To do this, you can create a new blank image with the desired size, paste the original image onto it, and save the new image. Here's an example:

```python
from PIL import Image

# Load the image
img = Image.open('image.jpg')

# Get the size of the image
width, height = img.size

# Create a new blank image with the same size as the original image
new_img = Image.new('RGB', (width, height), (255, 255, 255))

# Paste the original image onto the new image
new_img.paste(img, (0, 0))

# Save the new image
new_img.save('new_image.jpg')
```

In this example, we're creating a new blank image with the same size as the original image, filling it with white pixels, pasting the original image onto it, and then saving the new image.

## Conclusion
In this tutorial, we've seen two ways to remove unwanted white space around an image in Python. Depending on your use case, one option may be more suitable than the other. Use these methods to remove the border from your images and create a cleaner, more professional look.
