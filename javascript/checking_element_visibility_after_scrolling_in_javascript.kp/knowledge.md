---
title: What is the procedure for determining if an element is visible after scrolling?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Check if the element`s position relative to the viewport is within the visible area using the Element.getBoundingClientRect() method.
---

**Contents**

[TOC]

### Step 1: Get the Element

The first step is to get the element you want to check for visibility. This can be done with document.querySelector() or document.getElementById():

```javascript
var myElement = document.querySelector("#myElement");
```

### Step 2: Get the Element's Position

Once you have the element, you need to get its position on the page. This can be done with the getBoundingClientRect() method:

```javascript
var elementPosition = myElement.getBoundingClientRect();
```

### Step 3: Compare the Element's Position to the Viewport

Next, you need to compare the element's position to the viewport. This can be done with the window.innerHeight and window.innerWidth properties:

```javascript
if (elementPosition.top > 0 && elementPosition.left > 0 && elementPosition.bottom < window.innerHeight && elementPosition.right < window.innerWidth) {
    // Element is visible
}
```

### Step 4: Check for Visibility

Finally, you can check for visibility by comparing the element's position to the viewport. If the element is within the viewport, it is visible.
