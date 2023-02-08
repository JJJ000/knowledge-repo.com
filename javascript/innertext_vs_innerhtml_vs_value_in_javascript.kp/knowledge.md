---
title: What is the distinction between innertext, innerhtml, and value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: innerText returns the visible text content of an element, innerHTML returns the HTML content of an element, and value returns the value of an element (such as an input field).
---

**Contents**

[TOC]

### innerText
innerText is a property of a DOM element that returns a string of all the text content inside of it. It is not affected by any styling or formatting, so the text returned is the same as what is seen on the page.

### innerHTML
innerHTML is a property of a DOM element that returns a string of all the HTML content inside of it. This includes any HTML tags and styling associated with the content.

### value
value is a property of a DOM element that returns a string of the current value of the element. This is typically used with form elements such as input fields, select boxes, and textareas.
