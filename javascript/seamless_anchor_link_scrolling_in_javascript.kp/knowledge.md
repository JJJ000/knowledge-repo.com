---
title: Scrolling seamlessly when clicking a link to a specific section of a page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To enable smooth scrolling when clicking an anchor link in Javascript, use the `scrollIntoView()` method.
---

**Contents**

[TOC]

# Introduction
Smooth scrolling is a technique used to create a more seamless transition when navigating to a different section on a webpage. It is often used when clicking an anchor link, which is a link that points to a specific section on the page. Smooth scrolling can be achieved in JavaScript by using the window.scrollTo() method.

# Syntax
The syntax for the window.scrollTo() method is as follows:

window.scrollTo(x-coordinate, y-coordinate)

The x-coordinate and y-coordinate parameters specify the position on the page to which the browser should scroll.

# Example
For example, if you have an anchor link with the id "myAnchor" and you want to scroll to it when it is clicked, you could use the following code:

```javascript
document.getElementById('myAnchor').addEventListener('click', function() {
  window.scrollTo(0, document.getElementById('myAnchor').offsetTop);
});
```

# Conclusion
In conclusion, smooth scrolling can be achieved in JavaScript using the window.scrollTo() method. By passing the x-coordinate and y-coordinate parameters, you can specify the position on the page to which the browser should scroll when an anchor link is clicked.
