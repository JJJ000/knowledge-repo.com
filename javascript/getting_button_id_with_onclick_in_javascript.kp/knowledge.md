---
title: When the button is clicked, retrieve its id
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the event object`s `target` property to get the ID of the clicked button.
---

**Contents**

[TOC]

### Using Event Listener

To get the ID of the clicked button using an event listener, we can use the `addEventListener` method.

```javascript
let btn = document.querySelector('#myButton');

btn.addEventListener('click', function(e) {
  let clickedButtonId = e.target.id;
  console.log(clickedButtonId);
});
```

### Using onclick Event Handler

We can also use the `onclick` event handler to get the ID of the clicked button:

```javascript
let btn = document.querySelector('#myButton');

btn.onclick = function(e) {
  let clickedButtonId = e.target.id;
  console.log(clickedButtonId);
};
```
