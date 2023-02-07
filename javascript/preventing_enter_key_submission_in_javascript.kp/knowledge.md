---
title: Stop form submission when enter key is pressed
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Prevent form submission on Enter key press by adding an event listener to the form and calling the preventDefault() method on the event.
---

**Contents**

[TOC]

# Solution 1

Using `event.preventDefault()`:

```javascript
document.addEventListener("keydown", function(event) {
  if (event.keyCode == 13) {
    event.preventDefault();
  }
});
```

# Solution 2

Using `return false`:

```javascript
document.addEventListener("keydown", function(event) {
  if (event.keyCode == 13) {
    return false;
  }
});
```
