---
title: What is the jquery code for the escape key?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The keycode for the escape key with jQuery in Javascript is 27.
---

**Contents**

[TOC]

1. Syntax

```
$(document).keydown(function(e) {
    if (e.keyCode == 27) {
        // Do something
    }
});
```

2. KeyCode

The keycode for the escape key is `27`.

3. Usage

This code can be used to detect when the escape key is pressed and execute a certain action.

4. Notes

It is important to note that this code only works when the document is in focus.
