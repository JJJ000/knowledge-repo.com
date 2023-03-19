---
title: Rephrase "change the format of an image from pil to opencv."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the cv2.cvtColor() function to convert a PIL image to the openCV format in Python.
---

**Contents**

[TOC]

## Installing the Required Libraries

The first step in converting an image from PIL format to OpenCV format in Python is to install the required libraries. The two main libraries needed for this conversion are `Pillow` (Python Imaging Library fork) and `OpenCV` (Open Source Computer Vision Library). If these libraries are not installed on your machine, you can install them using `pip` or `conda`.

The following command can be used to install these libraries using pip:

```
pip install Pillow
pip install opencv-python
```

Or you can install these libraries using conda as well:

```
conda install pillow
conda install opencv
```


## Converting an Image from PIL to OpenCV format

After installing the required libraries, we can write the code to convert an image from PIL to OpenCV format. First, we need to import the necessary libraries (`cv2` for OpenCV and `PIL` for PIL).

```python
import cv2
from PIL import Image
```

Next, we load the image using PIL's `Image.open()` method and convert it to OpenCV's format using the `cv2.cvtColor()` method. 

```python
#load the image using PIL
pil_image = Image.open('image.jpg')

#convert the image to an OpenCV format
open_cv_image = cv2.cvtColor(np.array(pil_image), cv2.COLOR_RGB2BGR)
```


## Saving the Converted Image

Finally, we can save the converted image using the `cv2.imwrite()` method. 

```python
#save the converted image
cv2.imwrite('image_opencv.jpg', open_cv_image)
```

The above code will save the converted image in the current directory with the name `image_opencv.jpg`. 

And that's it! We have successfully converted an image from PIL format to OpenCV format using Python.
