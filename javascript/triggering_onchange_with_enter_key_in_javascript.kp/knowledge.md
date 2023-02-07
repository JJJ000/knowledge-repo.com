---
title: Trigger the onchange event when the enter key is pressed
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Call the onChange event handler when the Enter key is pressed.
---

**Contents**

[TOC]

## Adding Event Listener

The first step to calling an `onChange` event after pressing the enter key is to add an event listener to the element. This can be done by using the `addEventListener` method. The syntax for this is as follows:

```js
element.addEventListener('keydown', function(event) {
  // code to be executed
});
```

## Checking for Enter Key

Once the event listener is added, the next step is to check if the enter key has been pressed. This can be done by checking the `event.keyCode` property. If the value is `13`, then the enter key has been pressed. 

```js
element.addEventListener('keydown', function(event) {
  if (event.keyCode === 13) {
    // code to be executed
  }
});
```

## Calling the onChange Event

Once the enter key is detected, then the `onChange` event can be called. This can be done by using the `dispatchEvent` method. The syntax for this is as follows:

```js
element.addEventListener('keydown', function(event) {
  if (event.keyCode === 13) {
    element.dispatchEvent(new Event('change'));
  }
});
```

## Adding the onChange Event Listener

Finally, the last step is to add an event listener for the `onChange` event. This can be done by using the `addEventListener` method. The syntax for this is as follows:

```js
element.addEventListener('change', function() {
  // code to be executed
});
```
