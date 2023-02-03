---
title: The difference between window.onload and $(document).ready() in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: window.onload waits for all content on the page to load before executing, while $(document).ready() executes as soon as the DOM is ready.
---

**Contents**

[TOC]

**window.onload**

- Definition: 
window.onload is a JavaScript event that fires when the entire page has loaded, including all dependent resources such as stylesheets and images.

- Usage:
window.onload is typically used to perform tasks that require all page content to be loaded, such as setting up a JavaScript-based image gallery or ad rotator.

**$(document).ready()**

- Definition:
$(document).ready() is a jQuery event that fires when the DOM is ready for JavaScript code to execute.

- Usage:
$(document).ready() is typically used to perform tasks that do not require all page content to be loaded, such as attaching event handlers to elements or initializing a JavaScript plugin.
