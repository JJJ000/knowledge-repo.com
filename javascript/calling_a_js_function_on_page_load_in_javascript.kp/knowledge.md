---
title: What is the syntax for running a JavaScript function when the page loads?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can call a JavaScript function on page load by using the window.onload event.
---

**Contents**

[TOC]

## Option 1: Using the onload Event

The onload event can be used to check the visitor's browser type and browser version, and load the proper version of the web page based on the information.

```javascript
window.onload = function(){
   //Your code here
};
```

## Option 2: Using the jQuery Ready Function

The jQuery ready function allows you to execute code when the document is fully loaded.

```javascript
$(document).ready(function(){
   //Your code here
});
```

## Option 3: Using the JavaScript addEventListener Function

The addEventListener function can be used to execute code when the document is fully loaded.

```javascript
document.addEventListener("DOMContentLoaded", function(event) {
   //Your code here
});
```

## Option 4: Using the HTML Tag onload Attribute

The onload attribute can be used to execute a script when an element is loaded.

```html
<body onload="myFunction()">
   <!-- content -->
</body>
```
