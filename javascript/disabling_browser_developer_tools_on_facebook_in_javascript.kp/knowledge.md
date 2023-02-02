---
title: What steps does facebook take to deactivate the in-built developer tools in a web browser?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Facebook uses the Javascript function `window.onerror` to override and disable the browser`s integrated Developer Tools.
---

**Contents**

[TOC]

1. Using `window.onerror` 

Facebook uses the `window.onerror` method to detect and prevent access to the browser's integrated Developer Tools. This method allows Facebook to detect when a user attempts to open the Developer Tools, and then take the necessary steps to disable them.

2. Using `window.addEventListener`

Facebook also uses the `window.addEventListener` method to detect when a user attempts to open the Developer Tools. This method allows Facebook to detect the key combination used to open the Developer Tools and take the necessary steps to disable them.

3. Using `document.addEventListener`

Facebook also uses the `document.addEventListener` method to detect when a user attempts to open the Developer Tools. This method allows Facebook to detect the mouse click used to open the Developer Tools and take the necessary steps to disable them.

4. Using `document.onkeydown`

Facebook also uses the `document.onkeydown` method to detect when a user attempts to open the Developer Tools. This method allows Facebook to detect the keyboard shortcut used to open the Developer Tools and take the necessary steps to disable them.
