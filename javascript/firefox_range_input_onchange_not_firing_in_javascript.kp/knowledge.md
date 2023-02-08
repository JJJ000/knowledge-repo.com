---
title: The 'onchange' event is not being activated when dragging the slider of an input type=range element in firefox
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The onchange event is not triggered in Firefox until the input type=range is released.
---

**Contents**

[TOC]

### Solution

#### Adding an Event Listener

Adding an event listener to the `input` element with the `change` event should solve the problem.

```javascript
document.querySelector('input[type="range"]').addEventListener('change', () => {
  // Do something
});
```

#### Using the oninput Event

Alternatively, the `oninput` event can be used instead of the `change` event.

```javascript
document.querySelector('input[type="range"]').oninput = () => {
  // Do something
};
```

#### Using the onchange Event

If the `oninput` event still does not work, then the `onchange` event can be used.

```javascript
document.querySelector('input[type="range"]').onchange = () => {
  // Do something
};
```

#### Using the onchange Event with setTimeout

Finally, if all else fails, the `onchange` event can be used with `setTimeout`.

```javascript
document.querySelector('input[type="range"]').onchange = () => {
  setTimeout(() => {
    // Do something
  }, 100);
};
```
