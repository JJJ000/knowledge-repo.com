---
title: Altering the color of an Android floating action button
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The color of a Floating Action Button can be changed programmatically using the setBackgroundTintList() method.
---

**Contents**

[TOC]

1. Create a Color State List
--------------------------------
A color state list is an XML file that specifies colors for different states of a View. To create a color state list, create an XML file in your project's `res/color` directory.

2. Create a Drawable
--------------------
A drawable is a class that wraps a color state list and can be used as a background for a Floating Action Button. To create a drawable, create an XML file in your project's `res/drawable` directory.

3. Set the Drawable as the Floating Action Button's Background
----------------------------------------------------------------
To set the drawable as the background for a Floating Action Button, call the `setBackgroundDrawable()` method on the Floating Action Button instance.

4. Change the Color State List
------------------------------
To change the color state list, edit the XML file in your project's `res/color` directory. The color state list specifies the colors for different states of a View.
