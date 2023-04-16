---
title: Comparing the events of onkeypress, onkeyup and onkeydown
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: onKeyPress is triggered when a key is pressed, onKeyUp is triggered when a key is released, and onKeyDown is triggered when a key is first pressed.
---

**Contents**

[TOC]

### onKeyPress

`onKeyPress` is an event handler that is triggered when a key is pressed down on the keyboard. It is supported by all major browsers. The handler will be triggered for all keys, including special characters, numbers, and letters. This event handler is useful for capturing user input and responding to it in real-time.

### onKeyUp and onKeyDown

`onKeyUp` and `onKeyDown` are event handlers that are triggered when a key is pressed down and released, respectively. These handlers are useful for capturing user input and responding to it after the key has been released. Unlike `onKeyPress`, these handlers are not triggered for special characters, numbers, and letters.
