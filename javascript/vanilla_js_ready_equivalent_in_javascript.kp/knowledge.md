---
title: The domcontentloaded event is the equivalent without jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: document.addEventListener(`DOMContentLoaded`, function() { //code });
---

**Contents**

[TOC]

### Vanilla JavaScript

Vanilla JavaScript is a term for JavaScript that does not include any additional libraries or frameworks.

### Document Ready

To achieve the same functionality as the jQuery `$(document).ready()` method, you can use the `DOMContentLoaded` event. This event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.

```
document.addEventListener('DOMContentLoaded', function() {
  // code goes here
});
```

### Other Options

You can also use the `load` event, which is fired when the entire page has loaded, including all dependent resources such as stylesheets and images.

```
window.addEventListener('load', function() {
  // code goes here
});
```

Finally, you can use the `DOMContentLoaded` event on modern browsers and a `readystatechange` event for older browsers.

```
document.onreadystatechange = function () {
  if (document.readyState === "complete") {
    // code goes here
  }
};
```
