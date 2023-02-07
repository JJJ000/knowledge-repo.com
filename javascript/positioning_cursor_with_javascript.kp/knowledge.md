---
title: Place the cursor at the end of the text in a text input element using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the .focus() method and the .setSelectionRange() method on the text input element to place the cursor at the end of the text.
---

**Contents**

[TOC]

**Solution 1:**

Using `setSelectionRange()`

```javascript
let el = document.getElementById("myInput");
el.focus();
el.setSelectionRange(el.value.length, el.value.length);
```

**Solution 2:**

Using `createTextRange()`

```javascript
let el = document.getElementById("myInput");
let range = el.createTextRange();
range.collapse(false);
range.select();
```
