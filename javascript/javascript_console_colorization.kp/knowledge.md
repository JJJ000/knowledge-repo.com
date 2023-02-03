---
title: Modifying colors in the JavaScript console
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The colors in the JavaScript console are black text on a white background.
---

**Contents**

[TOC]

# Section 1: Console Logging
The most common way to output text to the console is to use the `console.log()` function. This function allows you to pass in any data type and will output the data to the console.

# Section 2: Color Output
The `console.log()` function can also be used to output colored text to the console. This is done by using the `%c` placeholder and passing in a string with a color value.

# Section 3: Color Values
The color value string takes the format of `color: <color-name>;` and can be used to set the color of the text output. The available color names are `black`, `red`, `green`, `yellow`, `blue`, `magenta`, `cyan`, and `white`.

# Section 4: Example
For example, the following code will output the text "Hello World!" in green to the console: 
```
console.log('%cHello World!', 'color: green;');
```
