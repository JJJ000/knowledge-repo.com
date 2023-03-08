---
title: What is the process for displaying a pil image in an ipython notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the following code snippet `from IPython.display import Image; Image(filename=`<path\_to\_image>`)` to show PIL image in ipython notebook.
---

**Contents**

[TOC]

## Section 1: Load the PIL Image

The first step is to load the PIL image using the `Image` module from PIL. This can be done by specifying the path of the image file as shown below:

```python
from PIL import Image

im = Image.open("image.jpg")
```

## Section 2: Display the PIL Image

Once the PIL image is loaded, it can be displayed using the `imshow()` function from the Matplotlib library. This function takes the PIL image object as input and displays it in the current plot.

```python
import matplotlib.pyplot as plt

plt.imshow(im)
```

Alternatively, if you prefer to display the image inline within the notebook, you can use the `%matplotlib inline` magic command before calling `imshow()`:

```python
%matplotlib inline

import matplotlib.pyplot as plt

plt.imshow(im)
```

## Section 3: Resize the Image

Sometimes, the image may be too large to display properly in the notebook. In such cases, you can resize the image before displaying it using the `resize()` function from PIL.

```python
from PIL import Image

im = Image.open("image.jpg")
im_resized = im.resize((500, 500))   # resize to 500x500 pixels

import matplotlib.pyplot as plt

plt.imshow(im_resized)
```

## Section 4: Save the Displayed Image

If you want to save the displayed image, you can use the `savefig()` function from Matplotlib. This function takes the file path as input and saves the displayed image to that path.

```python
import matplotlib.pyplot as plt

# display image
plt.imshow(im_resized)

# save image to file
plt.savefig("image_displayed.png")
```
