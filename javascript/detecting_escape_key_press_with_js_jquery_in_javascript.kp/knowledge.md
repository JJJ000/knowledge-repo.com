---
title: What is the best way to identify when the escape key has been pressed using either JavaScript or jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Using jQuery, the escape key press can be detected with the $(document).on(`keyup`, function(e) { if (e.keyCode == 27) { /* Escape key pressed */ } }); syntax.
---

**Contents**

[TOC]

### Using Pure JavaScript

1. Add an event listener to the window object for the `keydown` event.
2. Inside the event listener callback function, check the `event.key` property to determine if the key pressed was the Escape key.
3. If the key pressed was the Escape key, execute the desired code.

### Using jQuery

1. Add an event listener to the `document` object for the `keydown` event.
2. Inside the event listener callback function, check the `event.which` property to determine if the key pressed was the Escape key.
3. If the key pressed was the Escape key, execute the desired code.
