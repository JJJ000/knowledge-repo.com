---
title: Is there a way to determine if a scrollbar is visible?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can check if a scrollbar is visible by checking the scrollHeight and clientHeight of an element.
---

**Contents**

[TOC]

### Using jQuery

The following code snippet can be used to check if a scrollbar is visible using jQuery:

```javascript
if ($('body').height() > $(window).height()) {
    // scrollbar is visible
} else {
    // scrollbar is not visible
}
```

### Using Vanilla JavaScript

The following code snippet can be used to check if a scrollbar is visible using vanilla JavaScript:

```javascript
if (document.body.scrollHeight > window.innerHeight) {
    // scrollbar is visible
} else {
    // scrollbar is not visible
}
```

### Using CSS

The following code snippet can be used to check if a scrollbar is visible using CSS:

```css
body {
    overflow-y: scroll;
}
```

If the body element has a scrollbar visible, the above CSS will be applied.
