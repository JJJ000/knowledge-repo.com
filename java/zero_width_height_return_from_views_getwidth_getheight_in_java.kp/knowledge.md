---
title: The output of view's getwidth() and getheight() is 0
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This is because the View has not been measured and laid out yet.
---

**Contents**

[TOC]

### Explanation

When a View is created, its width and height are not immediately known. The width and height of a View is determined by its parent, which is usually a ViewGroup. The ViewGroup will measure the View and assign it a width and height. Until this measurement is completed, the View's getWidth() and getHeight() methods will return 0.

### Solution

In order to ensure that the View's width and height are correctly measured, the View must be added to its parent before attempting to retrieve the width and height. This can be done by calling the parent's addView() method.

### Further Reading

For more information on how Views are measured and laid out, see the Android documentation on [Measurement and Layout](https://developer.android.com/guide/topics/ui/measurement-and-layout).
