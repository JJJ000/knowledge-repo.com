---
title: Window.onload and document.onload are both events that are triggered when the page is finished loading. the difference between the two is that window.onload will only fire after all the page's content (images, scripts, etc.) is loaded, while document.onload will fire as soon as the dom is ready
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: window.onload fires after the entire page has been loaded, while document.onload fires only after the DOM has been loaded.
---

**Contents**

[TOC]

### window.onload

`window.onload` is a JavaScript event that fires when the entire page (HTML) has loaded, including all dependent resources such as stylesheets and images. It is a good place to have scripts that need to access DOM elements or set up event handlers.

### document.onload

`document.onload` is not a valid event in JavaScript. It is likely a typo of `document.ready`, which is a jQuery event that fires when the DOM is ready to be manipulated. It is a good place to have scripts that need to access DOM elements or set up event handlers.
