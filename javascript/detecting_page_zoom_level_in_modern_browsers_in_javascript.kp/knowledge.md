---
title: What is the best way to determine the page zoom level in all current web browsers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The zoom level of a page can be detected in all modern browsers using the window.devicePixelRatio property.
---

**Contents**

[TOC]

# Section 1 - Detecting Zoom Level in Chrome

In Chrome, the zoom level of the page can be detected using the `window.devicePixelRatio` property. This property returns the ratio between the current display resolution and the reference resolution. 

# Section 2 - Detecting Zoom Level in Firefox

In Firefox, the zoom level of the page can be detected using the `window.mozInnerScreenX/Y` properties. This property returns the ratio between the current display resolution and the reference resolution.

# Section 3 - Detecting Zoom Level in Internet Explorer

In Internet Explorer, the zoom level of the page can be detected using the `document.body.getBoundingClientRect()` method. This method returns the width and height of the page in the current zoom level.

# Section 4 - Detecting Zoom Level in Safari

In Safari, the zoom level of the page can be detected using the `window.innerWidth/Height` properties. This property returns the ratio between the current display resolution and the reference resolution.
