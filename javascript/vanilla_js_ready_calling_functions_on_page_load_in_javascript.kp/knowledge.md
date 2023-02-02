---
title: How to call a function when the page/dom is ready for it using vanilla JavaScript equivalent of jquery's $.ready()
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The DOMContentLoaded event can be used to call a function when the page/DOM is ready for it in Javascript.
---

**Contents**

[TOC]

### Using the DOMContentLoaded Event
The DOMContentLoaded event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.

```
document.addEventListener('DOMContentLoaded', function() {
  // your code here
});
```

### Using the load Event
The load event is fired when the whole page has loaded, including all dependent resources such as stylesheets and images.

```
window.addEventListener('load', function() {
  // your code here
});
```

### Using the onload Attribute
The onload attribute is an event attribute supported by all major browsers. It is fired when the whole page has loaded, including all dependent resources such as stylesheets and images.

```
<body onload="myFunction()">
  ...
</body>
```

### Using the setTimeout Function
The setTimeout function can be used to delay the execution of a function until the page has finished loading.

```
setTimeout(function(){
  // your code here
}, 0);
```
