---
title: What is the process for temporarily disabling scrolling?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `document.body.style.overflow = `hidden`` command to temporarily disable scrolling in Javascript.
---

**Contents**

[TOC]

# Section 1: Disable Scrolling

1. Store the current scroll position of the window:
```javascript
var currentScrollPosition = window.pageYOffset;
```

2. Set the scroll position of the window to the top:
```javascript
window.scrollTo(0, 0);
```

# Section 2: Enable Scrolling

1. Set the scroll position of the window to the stored position:
```javascript
window.scrollTo(0, currentScrollPosition);
```

# Section 3: Prevent Default Scrolling

1. Add an event listener for the scroll event:
```javascript
window.addEventListener('scroll', function(event) {
    event.preventDefault();
});
```

# Section 4: Remove Event Listener

1. Remove the event listener for the scroll event:
```javascript
window.removeEventListener('scroll', function(event) {
    event.preventDefault();
});
```
