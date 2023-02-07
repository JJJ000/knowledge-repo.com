---
title: Verify that an element is not present using cypress
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if an element does not exist in Javascript by using the `!document.querySelector()` method.
---

**Contents**

[TOC]

##### Using Vanilla JavaScript

1. Use `document.querySelector` to search for the element. 
2. If the query returns `null`, the element does not exist in the DOM.

##### Using jQuery

1. Use `$(selector)` to search for the element. 
2. If the query returns an empty array, the element does not exist in the DOM.
