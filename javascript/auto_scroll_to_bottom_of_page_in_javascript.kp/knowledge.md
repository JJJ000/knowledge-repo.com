---
title: Scroll to the end of the page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: window.scrollTo(0,document.body.scrollHeight);
---

**Contents**

[TOC]

# Section 1 - Setting up the Page

The first step to automatically scrolling to the bottom of the page in JavaScript is to set up the page. This involves creating a div element and setting its height and width to the size of the page. Additionally, the page should be set to overflow-y: scroll, which will allow the page to scroll when the user scrolls.

# Section 2 - Creating the JavaScript Function

The next step is to create a JavaScript function that will be called when the page is loaded. This function should set the scrollTop property of the div element to the height of the page. This will cause the page to automatically scroll to the bottom when it is loaded.

# Section 3 - Calling the JavaScript Function

The last step is to call the JavaScript function when the page is loaded. This can be done using the window.onload event. This event will be triggered when the page is finished loading, and the JavaScript function can be called at this point.

# Section 4 - Testing the Automatically Scrolling

Once the JavaScript function is set up and called, the page should automatically scroll to the bottom when it is loaded. To test this, simply reload the page and observe if it automatically scrolls to the bottom. If it does, then the automatically scrolling has been successfully set up.
