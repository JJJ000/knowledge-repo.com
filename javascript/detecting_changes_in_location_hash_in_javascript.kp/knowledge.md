---
title: What is the best way to identify alterations in the location hash?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can detect changes in location hash in Javascript by listening for the `hashchange` event.
---

**Contents**

[TOC]

1. Using the `window.onhashchange` Event
---------------------------------------
The `window.onhashchange` event is fired when the fragment identifier of the URL has changed (the part of the URL that comes after the # symbol). This event can be used to detect changes in the location hash.

2. Using the `window.location.hash` Property
------------------------------------------------
The `window.location.hash` property can be used to detect changes in the location hash. The property is updated when the fragment identifier of the URL has changed.

3. Using the `window.addEventListener` Method
------------------------------------------------
The `window.addEventListener` method can be used to detect changes in the location hash. The method takes a string representing the event type as its first argument and a callback function as its second argument. The callback function will be called when the event type specified in the first argument is triggered.

4. Using the `window.onpopstate` Event
---------------------------------------
The `window.onpopstate` event is fired when the user navigates through the history (i.e. when the user clicks the back or forward button). This event can be used to detect changes in the location hash.
