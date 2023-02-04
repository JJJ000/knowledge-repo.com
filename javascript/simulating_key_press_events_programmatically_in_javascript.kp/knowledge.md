---
title: Can key press events be simulated with a program?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Yes, it is possible to simulate key press events programmatically in Javascript using the `keydown` or `keyup` event.
---

**Contents**

[TOC]

**Yes, It Is Possible**

**Using the `keydown` Event**

The `keydown` event is fired when a key on the keyboard is pressed. This event can be used to programmatically simulate a key press. The `keydown` event accepts an object with a `key` property that indicates which key was pressed.

For example, the following code simulates a `Space` key press:

```javascript
document.addEventListener('keydown', (event) => {
  if (event.key === 'Space') {
    // Do something...
  }
});
```

**Using the `dispatchEvent` Method**

The `dispatchEvent` method can be used to programmatically simulate a key press. This method accepts an event object with a `key` property that indicates which key was pressed.

For example, the following code simulates a `Space` key press:

```javascript
const event = new KeyboardEvent('keydown', { key: 'Space' });
document.dispatchEvent(event);
```
