---
title: Jquery event to initiate an action when a div becomes visible
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The jQuery `show` event can be used to trigger an action when a div is made visible.
---

**Contents**

[TOC]

1. **Event Handler**

We can use the jQuery `.on()` method to bind an event handler to the `div` element when it is made visible. This event handler can be used to trigger a desired action.

```javascript
$("div").on("visible", function() {
    // Trigger action here
});
```

2. **Event Listener**

We can also use the `addEventListener()` method to add an event listener to the `div` element when it is made visible. This event listener can be used to trigger a desired action.

```javascript
document.getElementById("div").addEventListener("visible", function() {
    // Trigger action here
});
```

3. **Event Delegation**

We can use the jQuery `.on()` method with event delegation to bind an event handler to the parent element of the `div`. This event handler will be triggered when the `div` is made visible.

```javascript
$("parentElement").on("visible", "div", function() {
    // Trigger action here
});
```

4. **jQuery Visible Event**

We can use the jQuery `.visible()` event to bind an event handler to the `div` element when it is made visible. This event handler can be used to trigger a desired action.

```javascript
$("div").on("visible", function() {
    // Trigger action here
});
```
