---
title: How do I programmatically adjust the width and height of an imageview?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: ImageView.setLayoutParams(new LayoutParams(width, height));
---

**Contents**

[TOC]

`**` Set ImageView Width**

1. Get the ImageView object by calling `findViewById()` method.
2. Set the width and height of the ImageView object by calling `setLayoutParams()` method.
3. Pass `LayoutParams` object to `setLayoutParams()` method and set the width and height of the `LayoutParams` object.
4. Call `requestLayout()` method to update the view.

`**` Set ImageView Height**

1. Get the ImageView object by calling `findViewById()` method.
2. Set the width and height of the ImageView object by calling `setLayoutParams()` method.
3. Pass `LayoutParams` object to `setLayoutParams()` method and set the width and height of the `LayoutParams` object.
4. Call `requestLayout()` method to update the view.
