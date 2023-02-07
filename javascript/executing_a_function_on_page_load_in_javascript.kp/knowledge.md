---
title: What is the best way to call a function once the page has finished loading?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The window.onload event can be used to execute a function when the page has fully loaded.
---

**Contents**

[TOC]

### Using window.onload

The `window.onload` event can be used to execute a function when the page has fully loaded.

```javascript
window.onload = function() {
  // code to be executed
};
```

### Using document.addEventListener

The `document.addEventListener` method can be used to execute a function when the page has fully loaded.

```javascript
document.addEventListener('DOMContentLoaded', function () {
  // code to be executed
});
```

### Using jQuery

The `$(document).ready()` method can be used to execute a function when the page has fully loaded when using the jQuery library.

```javascript
$(document).ready(function(){
  // code to be executed
});
```
