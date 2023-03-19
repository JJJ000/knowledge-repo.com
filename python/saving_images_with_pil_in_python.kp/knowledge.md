---
title: Can you provide instructions on how to save an image using pil?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `save()` method of the PIL Image object, passing in the filename and desired file format as parameters.
---

**Contents**

[TOC]

## Installing PIL

First, you need to install the Python Imaging Library (PIL). This can be done by running the following command in your terminal:

```python
pip install pillow
```

## Opening and Saving an Image using PIL

Once you have installed PIL, you can use it to open and save images in Python. Here is an example of how to open an image using PIL:

```python
from PIL import Image

# Open the image file
with Image.open('image.jpg') as img:
    # do something with img object
```

To save an image using PIL, you can use the `save()` method. For example:

```python
from PIL import Image

# Open the image file
with Image.open('image.jpg') as img:
    # Rotate the image by 90 degrees
    img = img.rotate(90)
    # Save the new image
    img.save('rotated_image.jpg')
```

In this example, we first open the image using PIL and then rotate it by 90 degrees. Finally, we save the newly rotated image to a file named `rotated_image.jpg`.

## Saving Images in Different File Formats using PIL

PIL supports a wide range of file formats for saving images. To save an image in a specific file format, you can specify the format using the `format` parameter of the `save()` method. For example:

```python
from PIL import Image

# Open the image file
with Image.open('image.jpg') as img:
    # Rotate the image by 90 degrees
    img = img.rotate(90)
    # Save the new image in PNG format
    img.save('rotated_image.png', format='PNG')
```

In this example, we save the rotated image in PNG format instead of the default JPEG format. Other file formats that PIL supports include BMP, GIF, TIFF, and WEBP.

## Conclusion

In this tutorial, we have seen how to open, manipulate, and save images using the Python Imaging Library (PIL). PIL provides a wide range of functions and methods for working with images, making it a versatile tool for image processing tasks in Python.
