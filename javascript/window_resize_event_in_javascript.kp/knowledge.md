---
title: Javascript window resizing event
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The window resize event in JavaScript can be handled by the `onresize` event handler.
---

**Contents**

[TOC]

## Event Listener

The window resize event can be listened for with the `addEventListener` method. The `resize` event is fired when the document view (window) has been resized.

```javascript
window.addEventListener("resize", function(){
  // code to execute when the window is resized
});
```

## Throttling

When the window is resized, the `resize` event is fired multiple times in rapid succession. To prevent this from causing performance issues, the event should be throttled. This can be done with the `throttle` function.

```javascript
window.addEventListener("resize", throttle(function(){
  // code to execute when the window is resized
}, 250));
```

## Debouncing

Another way to prevent performance issues when the window is resized is to debounce the event. This can be done with the `debounce` function.

```javascript
window.addEventListener("resize", debounce(function(){
  // code to execute when the window is resized
}, 250));
```

## Event Object

The `resize` event also passes an event object to the callback function. This object contains information about the event, such as the window size.

```javascript
window.addEventListener("resize", function(e){
  console.log(e.target.innerWidth); // logs the window width
});
```
