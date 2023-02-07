---
title: What is the syntax for triggering a window resize event in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The window resize event can be triggered in JavaScript by calling the window.dispatchEvent() method with a new UIEvent object.
---

**Contents**

[TOC]

### Using addEventListener

The `addEventListener` method can be used to bind an event to the window object. This can be used to trigger the `resize` event. The syntax for this is as follows:

```javascript
window.addEventListener('resize', function() {
  // code to execute when window is resized
});
```

### Using dispatchEvent

The `dispatchEvent` method can be used to trigger a `resize` event on the window object. The syntax for this is as follows:

```javascript
window.dispatchEvent(new Event('resize'));
```

### Using jQuery

If jQuery is available, the `resize` event can be triggered using the `trigger` method. The syntax for this is as follows:

```javascript
$(window).trigger('resize');
```

### Using the window.onresize property

The `window.onresize` property can be used to set a function that will be called when the window is resized. This can be used to trigger the `resize` event. The syntax for this is as follows:

```javascript
window.onresize = function() {
  // code to execute when window is resized
};
```
