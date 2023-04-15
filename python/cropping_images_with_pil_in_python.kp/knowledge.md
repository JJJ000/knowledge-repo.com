---
title: What are the steps to crop an image with pil?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To crop an image using PIL in Python, use the crop() method with the desired dimensions or coordinates as arguments.
---

**Contents**

[TOC]

## Introduction
Pillow (PIL) is a popular open-source library in Python for image processing. It provides a wide range of functions to perform various image operations including cropping. Cropping is the process of removing unwanted parts of an image to focus on a specific area. Cropping can be useful in various applications such as object recognition, image annotation, and image compression. In this tutorial, we will discuss how to crop an image using PIL in Python.

## Loading Image
Before we can crop an image, we need to load it using the Image module from the PIL library. The Image module provides various methods to load images from files, streams, or URLs. Here we will load an image from a file.

```python
from PIL import Image

# Load the image from the file
image = Image.open("image.jpg")
```

## Cropping Image
The crop() method of the Image module is used to crop an image. It takes a tuple of four values as input representing the left, top, right, and bottom positions of the area to be cropped. The left and top positions specify the starting position, and the right and bottom positions specify the ending position of the area to be cropped. Here’s an example of how to crop a 100x100 pixels area from the top-left corner of the given image.

```python
# Crop the image
cropped_image = image.crop((0, 0, 100, 100))
```

## Saving Image
Finally, we can save the cropped image to a file using the save() method of the Image module. The save() method takes a filename as input and saves the image in that file format. Here’s an example of how to save the cropped image as a PNG file.

```python
# Save the cropped image
cropped_image.save("cropped_image.png")
``` 

## Conclusion
In this tutorial, we learned how to crop an image using PIL in Python. We loaded an image, cropped a specific area of that image, and saved the cropped image to a file. PIL provides many other image processing functions that can be used to enhance or modify the image further.
