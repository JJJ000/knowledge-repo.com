---
title: A JavaScript event listener that responds to clicks on a class
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can add a click event listener to a class in Javascript using the addEventListener() method.
---

**Contents**

[TOC]

### Syntax

```javascript
document.querySelector('.className').addEventListener('click', function() {
  // do something
});
```

### Explanation

The `document.querySelector('.className')` part of the code will select the element with the class name specified in the argument. Then, the `addEventListener()` method is used to attach an event listener to the selected element. The first argument of the `addEventListener()` method is the type of the event, in this case it is 'click'. The second argument is a callback function that will be called when the click event is triggered.

### Example

The following example will log 'Button clicked' to the console when the button with the class name 'btn' is clicked:

```javascript
document.querySelector('.btn').addEventListener('click', function() {
  console.log('Button clicked');
});
```
