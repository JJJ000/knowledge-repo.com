---
title: Random colour selector
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Math.random() can be used to generate a random number between 0 and 1, which can then be used to generate a random color in hexadecimal format.
---

**Contents**

[TOC]

### Math.random()

The most basic way to generate a random color in Javascript is to use the `Math.random()` function. This function will generate a random number between 0 and 1. This number can then be used to create a random color by assigning it to the red, green, and blue values of an RGB color.

### Using Hexadecimal

Another way to generate a random color in Javascript is to use a hexadecimal color code. This involves generating a random 6-digit hexadecimal number and using it to create a color. This can be done with the `Math.random()` function, as well as with other methods such as generating a random number between 0 and 16777215 (the maximum number of hexadecimal values).

### Using CSS

A third way to generate a random color in Javascript is to use CSS. The `background-color` property can be used to set a random color from a given set of colors. This can be done by assigning a random number to the `background-color` property, and then using the `color` function to set the color.

### Using a Library

Finally, there are several libraries available that can be used to generate random colors in Javascript. These libraries can be used to generate a wide variety of colors, including gradients, and they often provide additional features such as the ability to set the hue, saturation, and lightness of the generated color.
