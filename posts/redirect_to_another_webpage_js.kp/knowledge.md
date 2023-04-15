---
title: How can I redirect to a different webpage in JavaScript?
authors:
- smart_coder
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Assign a new value to `window.location` or use the `window.location.replace` method
---

**Contents**

[TOC]

### Assigning a new value to `windows.location`

To redirect to a different webpage in JavaScript, you can use the `window.location` object. You can assign a new value to `window.location` and this will navigate the user to the new page. For example:

```JS
window.location = "http://www.example.com";
```

This will redirect the user to http://www.example.com.

### Using the `window.location.replace` method

You can also use the `window.location.replace` function to navigate the user to a new page. This method is similar to assigning a new value to `window.location`, but it prevents the user from navigating back to the previous page using the browser's back button.

```JS
window.location.replace("http://www.example.com");
```

Note that both of these methods will replace the current page in the browser's history, so the user will not be able to use the back button to navigate back to the previous page.
