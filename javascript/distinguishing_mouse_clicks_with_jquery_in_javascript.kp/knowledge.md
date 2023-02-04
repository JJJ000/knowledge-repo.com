---
title: What is the difference between a left and right mouse click using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `event.which` property to distinguish between left and right mouse clicks in jQuery.
---

**Contents**

[TOC]

1. Detecting Left Mouse Click
--------------------------------
Using the `mousedown` event, you can detect a left mouse click by checking the `which` property of the event object. The `which` property is a numeric value that indicates the mouse button that was pressed. If the value is 1, then it is a left mouse click.

```javascript
$("#element").mousedown(function(e){
  if (e.which === 1) {
    // Left mouse button was clicked
  }
});
```

2. Detecting Right Mouse Click
--------------------------------
Using the `mousedown` event, you can detect a right mouse click by checking the `which` property of the event object. The `which` property is a numeric value that indicates the mouse button that was pressed. If the value is 3, then it is a right mouse click.

```javascript
$("#element").mousedown(function(e){
  if (e.which === 3) {
    // Right mouse button was clicked
  }
});
```

3. Cross-Browser Support
--------------------------------
The `which` property is not supported in Internet Explorer 8 and earlier. To ensure cross-browser compatibility, you can use the `button` property instead. The `button` property is a numeric value that indicates the mouse button that was pressed. If the value is 0, then it is a left mouse click, and if the value is 1, then it is a right mouse click.

```javascript
$("#element").mousedown(function(e){
  if (e.which === 1 || e.button === 0) {
    // Left mouse button was clicked
  }
  if (e.which === 3 || e.button === 1) {
    // Right mouse button was clicked
  }
});
```

4. Detecting Other Mouse Buttons
--------------------------------
The `which` and `button` properties can also detect other mouse buttons, such as the middle mouse button. The `which` property returns a value of 2 for the middle mouse button, and the `button` property returns a value of 1 for the middle mouse button.

```javascript
$("#element").mousedown(function(e){
  if (e.which === 2 || e.button === 1) {
    // Middle mouse button was clicked
  }
});
```
