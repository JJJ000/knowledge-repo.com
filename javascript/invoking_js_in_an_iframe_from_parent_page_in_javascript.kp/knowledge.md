---
title: Calling JavaScript code within an iframe from the parent page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The parent page can invoke JavaScript code in an iframe using the window.frames object.
---

**Contents**

[TOC]

# Section 1: Setting Up the Iframe

In order to invoke JavaScript code from an iframe, the iframe needs to be set up in the parent page. This can be done by creating an `<iframe>` element in the HTML of the parent page. The `src` attribute of the `<iframe>` element should be set to the URL of the page that contains the JavaScript code that needs to be invoked.

# Section 2: Accessing the Iframe

Once the iframe is set up in the parent page, the iframe can be accessed from the parent page using the `window.frames` object. The `window.frames` object is an array-like object that contains all of the iframes in the page. The iframe can be accessed by its index in the `window.frames` object.

# Section 3: Invoking the JavaScript Code

Once the iframe is accessed, the JavaScript code in the iframe can be invoked by using the `contentWindow` property of the iframe. The `contentWindow` property is a reference to the window object of the iframe. The JavaScript code in the iframe can then be invoked by using the `contentWindow.eval()` method. This method takes a string as an argument, which is the JavaScript code that needs to be invoked.

# Section 4: Example

Here is an example of how to invoke JavaScript code from an iframe:

```javascript
// Get the iframe from the window.frames object
var iframe = window.frames[0];

// Invoke the JavaScript code in the iframe
iframe.contentWindow.eval('alert("Hello World!")');
```
