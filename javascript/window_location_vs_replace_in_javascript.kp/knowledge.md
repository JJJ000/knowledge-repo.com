---
title: How do window.location= and window.location.replace() differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Window.location= assigns a new URL to the window object while window.location.replace() replaces the current URL with a new one.
---

**Contents**

[TOC]

##Functionality
Window.location= is used to assign a new URL to the window object. It will keep the previous URL in the session history, so the user can use the back button to navigate to it.

Window.location.replace() is also used to assign a new URL to the window object, but it will replace the current URL in the session history, so the user cannot use the back button to navigate to it.

##Performance
Window.location= will cause the browser to load the new page, but it will also save the current page in the session history. This can cause the browser to slow down due to the extra data being stored.

Window.location.replace() will also cause the browser to load the new page, but it will not save the current page in the session history. This can help the browser to run faster as it does not need to store extra data.

##Usage
Window.location= is generally used when the user needs to be able to navigate back to the previous page.

Window.location.replace() is generally used when the user does not need to be able to navigate back to the previous page.
