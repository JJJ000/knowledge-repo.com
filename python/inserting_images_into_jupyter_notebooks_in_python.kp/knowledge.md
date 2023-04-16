---
title: Adding an image to an ipython notebook using markdown
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To insert an image into IPython notebook markdown, use the `![Alt Text](Image URL)` syntax.
---

**Contents**

[TOC]

# Inserting an Image

To insert an image into an IPython notebook markdown, the following code can be used:

`![Alt Text](image_url)`

Where `image_url` is the URL of the image to be inserted.

# Specifying Image Size

It is also possible to specify the size of the image with the following code:

`<img src="image_url" width="width_in_pixels" height="height_in_pixels">`

Where `image_url` is the URL of the image to be inserted, `width_in_pixels` is the desired width of the image in pixels, and `height_in_pixels` is the desired height of the image in pixels.

# Adding a Caption

To add a caption to the image, the following code can be used:

`<figure>
  <img src="image_url" width="width_in_pixels" height="height_in_pixels">
  <figcaption>Caption Text</figcaption>
</figure>`

Where `image_url` is the URL of the image to be inserted, `width_in_pixels` is the desired width of the image in pixels, `height_in_pixels` is the desired height of the image in pixels, and `Caption Text` is the desired caption for the image.

# Aligning the Image

To align the image to the left, right, or center, the following code can be used:

`<div style="text-align:left/right/center">
  <img src="image_url" width="width_in_pixels" height="height_in_pixels">
  <figcaption>Caption Text</figcaption>
</div>`

Where `image_url` is the URL of the image to be inserted, `width_in_pixels` is the desired width of the image in pixels, `height_in_pixels` is the desired height of the image in pixels, `Caption Text` is the desired caption for the image, and `left/right/center` is the desired alignment of the image.
