---
title: What is the procedure to exit a browser tab?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the window.close() method to close the current tab in a browser window.
---

**Contents**

[TOC]

# Solution 1:

Using `window.close()`:

This method can be used to close the current tab in a browser window. It works by calling the `window.close()` method which will close the tab or window in which it is running.

# Solution 2:

Using `window.open()`:

This method can be used to close the current tab in a browser window. It works by using the `window.open()` method with the `_self` argument. This will open a new window with the same URL as the current window, but it will close the current tab when the new window is opened.

# Solution 3:

Using `window.location.replace()`:

This method can be used to close the current tab in a browser window. It works by using the `window.location.replace()` method with a blank URL. This will replace the current page with an empty page, which will close the current tab.

# Solution 4:

Using `history.go()`:

This method can be used to close the current tab in a browser window. It works by using the `history.go()` method with a negative value. This will move the browser's history back one page, which will close the current tab.
