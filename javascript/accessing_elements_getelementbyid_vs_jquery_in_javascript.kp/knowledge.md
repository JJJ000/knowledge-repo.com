---
title: Retrieving an element from the dom using document.getelementbyid versus using jquery's $() selector
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: document.getElementById is used to access the DOM element by its ID, while jQuery $() is used to access DOM elements using CSS selectors.
---

**Contents**

[TOC]

**document.getElementById()**
- Pros: 
    - This method is faster than jQuery's $() selector.
    - It is native to the browser, so it does not require any library or framework.

- Cons:
    - It can only select one element at a time.
    - It can only select elements by their ID.

**jQuery $()**
- Pros: 
    - This method is more powerful than document.getElementById(), as it can select multiple elements at once and can use multiple different selectors.
    - It is also cross-browser compatible, so it can be used on all modern browsers.

- Cons:
    - This method is slower than document.getElementById(), as it requires the jQuery library to be loaded.
    - It can be difficult to debug, as the code can be more complex.
