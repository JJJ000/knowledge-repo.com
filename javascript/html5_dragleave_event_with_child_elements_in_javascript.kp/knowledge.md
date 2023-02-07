---
title: The html5 dragleave event is triggered when the mouse cursor moves away from a child element while dragging
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, the dragleave event is only fired when the dragged element leaves the boundary of the target element.
---

**Contents**

[TOC]

### Overview
The HTML5 dragleave event is fired when the mouse leaves an element while dragging an item. This event is not fired when the mouse moves from one child element to another within the same parent element.

### How the Event Works
The dragleave event is fired when the mouse moves from one element to another element that is not a child of the original element. For example, if an element contains two child elements, dragging the mouse from one child element to the other will not fire the dragleave event.

### Browser Support
The dragleave event is supported in the latest versions of all major browsers.

### Examples
In the following example, the dragleave event is fired when the mouse moves from the parent element to any other element on the page.

```html
<div id="parent">
  <div id="child1">Child 1</div>
  <div id="child2">Child 2</div>
</div>

<script>
  document.getElementById('parent').addEventListener('dragleave', function(e) {
    console.log('Dragleave event fired!');
  });
</script>
```
