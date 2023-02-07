---
title: Resize the iframe so that its contents are displayed correctly
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The iframe`s width and height can be adjusted by setting its `width` and `height` attributes.
---

**Contents**

[TOC]

# Option 1: Resize on Load

The following code uses the `onload` event to detect when the iframe has loaded and then resizes it to the content inside:

```javascript
window.onload = function(){
  var iframe = document.getElementById('iframeID');
  iframe.width = iframe.contentWindow.document.body.scrollWidth;
  iframe.height = iframe.contentWindow.document.body.scrollHeight;
}
```

# Option 2: Resize on Change

The following code uses the `onresize` event to detect when the iframe has been resized and then updates the width and height accordingly:

```javascript
window.onresize = function(){
  var iframe = document.getElementById('iframeID');
  iframe.width = iframe.contentWindow.document.body.scrollWidth;
  iframe.height = iframe.contentWindow.document.body.scrollHeight;
}
```

# Option 3: Resize on Scroll

The following code uses the `onscroll` event to detect when the iframe has been scrolled and then updates the width and height accordingly:

```javascript
window.onscroll = function(){
  var iframe = document.getElementById('iframeID');
  iframe.width = iframe.contentWindow.document.body.scrollWidth;
  iframe.height = iframe.contentWindow.document.body.scrollHeight;
}
```

# Option 4: Resize on Timer

The following code uses a timer to periodically check if the iframe has been resized and then updates the width and height accordingly:

```javascript
setInterval(function(){
  var iframe = document.getElementById('iframeID');
  iframe.width = iframe.contentWindow.document.body.scrollWidth;
  iframe.height = iframe.contentWindow.document.body.scrollHeight;
}, 500);
```
