---
title: What is the method of combining a transparent png image with another image using pil?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `paste()` method of PIL Image module, passing the transparent image and position as parameters to merge it with the other image.
---

**Contents**

[TOC]

## Importing libraries
The first step is to import the necessary libraries. In this case, we need `PIL` (Python Imaging Library) library in order to work with images in Python. 

```python
from PIL import Image
```

## Open and resize the images
Before merging the images, we need to open and resize them to the same dimensions to ensure they fit together properly. 

```python
# open the two images
img1 = Image.open('image1.png')
img2 = Image.open('image2.png')

# resize the first image to fit the dimensions of the second image
img1 = img1.resize(img2.size)
```

## Merge the images
To merge the images, we need to create a new `Image` object with the same dimensions as the second image. Then, we can use the `paste()` method to paste the first image onto the new image with the desired position.

```python
# create a new image with same dimensions as second image
new_img = Image.new('RGBA', img2.size, (0, 0, 0, 0))

# paste the first image onto the new image
new_img.paste(img1, (0, 0), img1)

# paste the second image over the first image
new_img.paste(img2, (0, 0), img2)

# show the merged image
new_img.show()
```

## Save the merged image
Finally, we can save the merged image using the `save()` method with desired file name and extension.

```python
# save the merged image
new_img.save('merged.png')
```
