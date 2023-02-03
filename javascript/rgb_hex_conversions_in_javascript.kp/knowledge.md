---
title: Converting from rgb to hexadecimal and from hexadecimal to rgb
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Hex to RGB can be done with the `parseInt` method, and RGB to hex can be done with the `toString(16)` method.
---

**Contents**

[TOC]

#### Hex to RGB

To convert a hexadecimal color value to an RGB color value, we can use the following JavaScript code:

```javascript
function hexToRGB(hex) {
    var result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);
    return result ? {
        r: parseInt(result[1], 16),
        g: parseInt(result[2], 16),
        b: parseInt(result[3], 16)
    } : null;
}
```

#### RGB to Hex

To convert an RGB color value to a hexadecimal color value, we can use the following JavaScript code:

```javascript
function rgbToHex(r, g, b) {
    return "#" + ((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1);
}
```
