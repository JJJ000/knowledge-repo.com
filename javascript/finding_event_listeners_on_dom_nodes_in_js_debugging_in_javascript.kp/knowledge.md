---
title: What is the process for locating event listeners attached to a dom node using JavaScript or when debugging?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: In JavaScript, event listeners on a DOM node can be found by using the `addEventListener()` method.
---

**Contents**

[TOC]

### Using JavaScript

1. Use the `addEventListener()` method on the DOM node to add an event listener. This will add the event listener to the node and allow you to access it for debugging. 
2. Inspect the DOM node with the `getEventListeners()` method. This will return an object containing all of the event listeners on the node.
3. Iterate through the object to check for the desired event listener.

### Using Debugging

1. Set a breakpoint on the DOM node using the browser's debugging tools.
2. When the breakpoint is hit, inspect the DOM node and check for the desired event listener.
3. If the event listener is found, debug the code to identify any issues.
