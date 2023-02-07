---
title: Navigate to a specific tab on page refresh or hyperlink using twitter bootstrap
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, it is possible to go to a specific tab on page reload or hyperlink in Javascript by using the Bootstrap`s show method.
---

**Contents**

[TOC]

### Solution 1: Using Javascript

You can use Javascript to go to a specific tab on page reload or hyperlink. To do this, you first need to add an ID attribute to the tab's anchor element. Then, you can use the `window.location.hash` property to get the hash value of the current URL. Finally, you can use the `document.getElementById()` method to get the element with the specified ID and click it.

### Solution 2: Using jQuery

You can also use jQuery to go to a specific tab on page reload or hyperlink. To do this, you first need to add an ID attribute to the tab's anchor element. Then, you can use the `$(window).hash()` method to get the hash value of the current URL. Finally, you can use the `$('#id')` selector to get the element with the specified ID and use the `.tab('show')` method to show the tab.

### Solution 3: Using Bootstrap's JavaScript API

You can also use Bootstrap's JavaScript API to go to a specific tab on page reload or hyperlink. To do this, you first need to add an ID attribute to the tab's anchor element. Then, you can use the `$('#id').tab('show')` method to show the tab with the specified ID.

### Solution 4: Using URL Parameters

You can also use URL parameters to go to a specific tab on page reload or hyperlink. To do this, you first need to add an ID attribute to the tab's anchor element. Then, you can use the `window.location.search` property to get the URL parameters. Finally, you can use the `document.getElementById()` method to get the element with the specified ID and click it.
