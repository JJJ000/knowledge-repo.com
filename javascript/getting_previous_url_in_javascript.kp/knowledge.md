---
title: What is the syntax for retrieving the previous url in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The previous URL can be retrieved using the window.history.back() method.
---

**Contents**

[TOC]

# Section 1: Using the document.referrer Property

The document.referrer property is a read-only property that returns the URL of the document that loaded the current document. This can be used to get the previous URL in JavaScript.

# Section 2: Using the window.history Object

The window.history object is a read-only object that contains the history of the current window. It can be used to get the previous URL in JavaScript by accessing the previous URL in the window.history.state object.

# Section 3: Using the window.location Object

The window.location object is a read-only object that provides information about the current URL. It can be used to get the previous URL in JavaScript by accessing the previous URL in the window.location.href object.

# Section 4: Using the window.document Object

The window.document object is a read-only object that contains the DOM tree of the current document. It can be used to get the previous URL in JavaScript by accessing the previous URL in the window.document.referrer object.
