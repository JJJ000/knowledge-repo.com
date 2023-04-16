---
title: What is the process for handling a redirect following a jquery ajax call?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the window.location.replace() method to redirect the browser to a new URL after the Ajax call is complete.
---

**Contents**

[TOC]

### Option 1: Using Location

The `location` object can be used to manage a redirect request after an Ajax call. The `location.href` property can be set to the desired URL to redirect the page.

### Option 2: Using Window.location

The `window.location` object can also be used to manage a redirect request after an Ajax call. The `window.location.href` property can be set to the desired URL to redirect the page.

### Option 3: Using Window.location.replace

The `window.location.replace()` method can be used to manage a redirect request after an Ajax call. This method replaces the current page with the desired URL, thus avoiding the need for a separate redirect.

### Option 4: Using Window.location.assign

The `window.location.assign()` method can also be used to manage a redirect request after an Ajax call. This method loads the desired URL in the current window, thus avoiding the need for a separate redirect.
