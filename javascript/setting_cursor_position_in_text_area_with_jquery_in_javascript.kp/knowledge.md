---
title: Change the position of the cursor in a text area using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery can set the cursor position in a text area using the .prop() method.
---

**Contents**

[TOC]

## Solution 1

Using `.setSelectionRange()`:

```javascript
let textarea = document.getElementById("textarea");
let pos = 5;
textarea.focus();
textarea.setSelectionRange(pos, pos);
```

## Solution 2

Using `.selectionStart` and `.selectionEnd`:

```javascript
let textarea = document.getElementById("textarea");
let pos = 5;
textarea.focus();
textarea.selectionStart = pos;
textarea.selectionEnd = pos;
```
