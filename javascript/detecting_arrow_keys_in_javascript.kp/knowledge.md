---
title: Identifying when arrow keys are pressed in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To detect arrow key presses in JavaScript, use the `keydown` event listener.
---

**Contents**

[TOC]

### Solution 1:

Using the `keydown` event, you can detect when an arrow key is pressed. The event object contains a `key` property that can be used to identify the key that was pressed.

```javascript
document.addEventListener('keydown', function(event) {
  if (event.key === 'ArrowUp' || event.key === 'ArrowDown' || event.key === 'ArrowLeft' || event.key === 'ArrowRight') {
    // arrow key was pressed
  }
});
```

### Solution 2:

You can use the `keyCode` property of the event object to detect arrow key presses. The `keyCode` property contains a numerical code that corresponds to the key that was pressed.

```javascript
document.addEventListener('keydown', function(event) {
  switch(event.keyCode) {
    case 37: // left arrow
      // left arrow was pressed
      break;
    case 38: // up arrow
      // up arrow was pressed
      break;
    case 39: // right arrow
      // right arrow was pressed
      break;
    case 40: // down arrow
      // down arrow was pressed
      break;
  }
});
```
