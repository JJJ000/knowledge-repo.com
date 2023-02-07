---
title: What does it mean to include 'return false' in a click event listener?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Adding `return false` to a click event listener in Javascript will prevent the default action of the click event from occurring.
---

**Contents**

[TOC]

### Prevent Default Action

Adding `return false` to a click event listener in Javascript will prevent the default action of the click event from occurring. This is useful for preventing undesired behaviors in the event listener, such as opening a link in a new window.

### Stop Propagation

In addition to preventing the default action, `return false` will also stop the event from propagating up the DOM tree. This is useful for preventing parent elements from also responding to the same event.

### Return Value

Finally, `return false` will also return a value of `false` to the calling function. This can be used to determine if the event was successfully handled.
