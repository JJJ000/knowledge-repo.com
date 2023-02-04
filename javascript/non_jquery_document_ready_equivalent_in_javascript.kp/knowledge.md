---
title: What is the JavaScript code equivalent of '$(document).ready()'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The non-jQuery equivalent of `$(document).ready()` in Javascript is `document.addEventListener(`DOMContentLoaded`, function() {});`.
---

**Contents**

[TOC]

### Vanilla Javascript

`document.addEventListener('DOMContentLoaded', function(){
    // Your code here
});`

### Internet Explorer

`document.onreadystatechange = function(){
    if (document.readyState == "complete") {
        // Your code here
    }
}`

### Older Browsers

`if (window.addEventListener) {
    window.addEventListener('load', function(){
        // Your code here
    }, false);
} else if (window.attachEvent) {
    window.attachEvent('onload', function(){
        // Your code here
    });
} else {
    window.onload = function(){
        // Your code here
    };
}`
