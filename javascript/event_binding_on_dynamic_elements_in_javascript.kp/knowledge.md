---
title: How to attach an event to elements created dynamically?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Event listeners can be attached to dynamically created elements using event delegation.
---

**Contents**

[TOC]

# Section 1: Overview

Event binding on dynamically created elements is a technique used to attach an event handler to an element that is not present in the DOM at the time the page is loaded. This is often necessary when creating elements dynamically with JavaScript.

# Section 2: Syntax

The syntax for binding an event to a dynamically created element is similar to binding an event to an existing element. The only difference is that the element must be selected using a different method.

For example, if you want to bind a click event to a button element that is created dynamically, you would use the following syntax:

```js
$(document).on('click', 'button', function() {
  // Do something
});
```

# Section 3: Benefits

Using event binding on dynamically created elements has several benefits. It allows you to attach event handlers to elements that are not present in the DOM at the time the page is loaded. This is especially useful for creating interactive web applications that require elements to be added or removed from the DOM dynamically.

# Section 4: Limitations

One of the main limitations of event binding on dynamically created elements is that it can be difficult to debug. Since the element is not present in the DOM at the time the page is loaded, it can be difficult to identify the source of the problem. Additionally, if the element is removed from the DOM after the event is bound, the event handler may no longer be triggered.
