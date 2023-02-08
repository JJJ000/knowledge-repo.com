---
title: What is the procedure for executing a function when the page is loaded?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To run a function when the page is loaded in Javascript, use the window.onload event.
---

**Contents**

[TOC]

1. Using `window.onload`
   
   The `window.onload` event is fired when the whole page has loaded, including all dependent resources such as stylesheets and images.
   
   ```javascript
   window.onload = function() {
     // your code here
   };
   ```

2. Using `document.ready`
   
   The `document.ready` event is fired when the DOM is ready for JavaScript code to execute.
   
   ```javascript
   $(document).ready(function() {
     // your code here
   });
   ```

3. Using `DOMContentLoaded`
   
   The `DOMContentLoaded` event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.
   
   ```javascript
   document.addEventListener('DOMContentLoaded', function() {
     // your code here
   });
   ```

4. Using `jQuery.ready`
   
   The `jQuery.ready` event is fired when the DOM is ready for JavaScript code to execute.
   
   ```javascript
   $(function() {
     // your code here
   });
   ```
