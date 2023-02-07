---
title: Prevent dropdown menu from closing when clicked inside
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Prevent the event from bubbling up to the dropdown menu`s parent element.
---

**Contents**

[TOC]

**Solution 1:**

Using `e.stopPropagation()`

1. Add an event listener to the dropdown menu that listens for a click.
2. Within the event listener, call `e.stopPropagation()` to prevent the event from propagating up the DOM tree.

**Solution 2:** 

Using `e.preventDefault()`

1. Add an event listener to the dropdown menu that listens for a click.
2. Within the event listener, call `e.preventDefault()` to prevent the default action from taking place.
