---
title: Load a url in a new tab instead of a new window
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use window.open(url, `\_blank`); to open a URL in a new tab in Javascript.
---

**Contents**

[TOC]

**Solution 1:**

Using `window.open()`

1. Create a new `window.open()` object with the desired URL as the argument.
2. Set the `windowName` argument to `_blank`.
3. Set the `target` attribute of the link to `_blank`.

**Solution 2:**

Using `window.open()` and `window.focus()`

1. Create a new `window.open()` object with the desired URL as the argument.
2. Set the `windowName` argument to `_blank`.
3. Set the `target` attribute of the link to `_blank`.
4. Call the `window.focus()` method on the newly opened window.
