---
title: Assigning functions to arrow keys using javascript/jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery`s keydown() event can be used to bind arrow keys.
---

**Contents**

[TOC]

## Using Event Listeners

To bind arrow keys using event listeners, use the following code:

```javascript
document.addEventListener('keydown', function(event) {
    if(event.keyCode == 37) {
        // Left Arrow
    }
    else if(event.keyCode == 38) {
        // Up Arrow
    }
    else if(event.keyCode == 39) {
        // Right Arrow
    }
    else if(event.keyCode == 40) {
        // Down Arrow
    }
});
```

## Using jQuery

To bind arrow keys using jQuery, use the following code:

```javascript
$(document).keydown(function(event) {
    if(event.keyCode == 37) {
        // Left Arrow
    }
    else if(event.keyCode == 38) {
        // Up Arrow
    }
    else if(event.keyCode == 39) {
        // Right Arrow
    }
    else if(event.keyCode == 40) {
        // Down Arrow
    }
});
```
