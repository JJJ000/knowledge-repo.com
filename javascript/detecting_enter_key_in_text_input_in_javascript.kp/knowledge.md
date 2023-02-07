---
title: Identify when the enter key is pressed in a text input field
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The Enter key can be detected in a text input field in Javascript using the `keydown` event listener.
---

**Contents**

[TOC]

**Solution 1: Using the `keydown` Event**

```javascript
document.getElementById("myInput").addEventListener("keydown", function(event) {
  if (event.keyCode === 13) {
    // Do something when Enter key is pressed
  }
});
```

**Solution 2: Using the `keypress` Event**

```javascript
document.getElementById("myInput").addEventListener("keypress", function(event) {
  if (event.which === 13) {
    // Do something when Enter key is pressed
  }
});
```

**Solution 3: Using the `keyup` Event**

```javascript
document.getElementById("myInput").addEventListener("keyup", function(event) {
  if (event.keyCode === 13) {
    // Do something when Enter key is pressed
  }
});
```

**Solution 4: Using the `input` Event**

```javascript
document.getElementById("myInput").addEventListener("input", function(event) {
  if (event.data === "\n") {
    // Do something when Enter key is pressed
  }
});
```
