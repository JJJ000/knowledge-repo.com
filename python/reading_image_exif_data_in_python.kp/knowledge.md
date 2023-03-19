---
title: How can I access the exif data of an image in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the `exifread` module in Python to read the exif data for an image.
---

**Contents**

[TOC]

## Installing Required Libraries

Before we can start reading exif data for an image, we need to install the required library. In Python, we can use the "Pillow" library to access exif data. To install this library, we can use pip. 

```python
!pip install Pillow
```


## Opening and Loading Image File

The first step to reading exif data for an image is to open and load the image. We can use the Image module of the Pillow library to achieve this.

```python
from PIL import Image

img = Image.open('image.jpg')  # replace 'image.jpg' with the path of your image file
```


## Reading Exif Data

With the image file loaded, we can now use the `img._getexif()` method to get exif data for the image. This method returns a dictionary containing exif tags and their corresponding values.

```python
exif_data = img._getexif()
```

However, this dictionary can be difficult to read and understand. Fortunately, we can use the ExifTags module of the Pillow library to decode the exif tags and provide more human-readable values.

```python
from PIL.ExifTags import TAGS

for tag_id, value in exif_data.items():
    tag = TAGS.get(tag_id, tag_id)
    print(f"{tag}: {value}")
```

In this code snippet, we are iterating over each item in the `exif_data` dictionary, getting the corresponding exif tag name from the `TAGS` dictionary, and printing both the tag name and its value in a human-readable format. 

Note that some exif tags may not be present in the image or may have no value. In this case, the value printed will be `None`.

By following these steps, you can read the exif data for any image using Python.
