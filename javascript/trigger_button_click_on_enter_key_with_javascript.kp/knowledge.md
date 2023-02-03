---
title: Trigger a JavaScript event when the enter key is pressed in a text box
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: document.getElementById(`buttonID`).onkeypress = function(e){if(e.keyCode == 13){document.getElementById(`buttonID`).click();}}
---

**Contents**

[TOC]

### Step 1: Create an Event Listener

We can use the `addEventListener()` method to attach an event listener to an element and listen for the `keydown` event. We can then use the `keyCode` property to check if the key pressed was the Enter key (`keyCode === 13`):

```javascript
document.getElementById("myTextBox").addEventListener("keydown", function(event) {
  if (event.keyCode === 13) {
    // Run code for the Enter key here
  }
});
```

### Step 2: Create a Click Event

Next, we can create a click event on the button we want to trigger. We can use the `createEvent()` method and set its type to `click`:

```javascript
var clickEvent = document.createEvent("MouseEvent");
clickEvent.initEvent("click", true, true);
```

### Step 3: Trigger the Button Click

Finally, we can use the `dispatchEvent()` method to trigger the button click:

```javascript
document.getElementById("myButton").dispatchEvent(clickEvent);
```

### Step 4: Put It All Together

Putting it all together, we can create a function that will trigger a button click when the Enter key is pressed in a text box:

```javascript
function triggerButtonClick(textBoxId, buttonId) {
  document.getElementById(textBoxId).addEventListener("keydown", function(event) {
    if (event.keyCode === 13) {
      var clickEvent = document.createEvent("MouseEvent");
      clickEvent.initEvent("click", true, true);
      document.getElementById(buttonId).dispatchEvent(clickEvent);
    }
  });
}

triggerButtonClick("myTextBox", "myButton");
```
