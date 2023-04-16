---
title: How can an iframe be resized to fit the content within it without using a scrollbar?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The iframe`s height can be set to `auto` to automatically adjust its height according to the contents.
---

**Contents**

[TOC]

### Option 1

Use `window.postMessage()` to send messages between the parent window and the iframe. The parent window can listen for messages from the iframe, and the iframe can listen for messages from the parent window.

The iframe should send a message to the parent window each time the content changes in the iframe. The parent window can then update the iframe's height accordingly.

### Option 2

Include a script in the iframe that measures the height of the content and sends the height back to the parent window. The parent window can then update the iframe's height accordingly.

### Option 3

Include a script in the iframe that continuously measures the height of the content and updates the iframe's height accordingly.

### Option 4

Use the `onload` event handler to detect when the iframe's content has finished loading. The `onload` event handler can then measure the height of the content and update the iframe's height accordingly.
