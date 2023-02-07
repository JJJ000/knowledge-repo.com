---
title: What is the syntax for having multiple $(document).ready functions in jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Multiple $(document).ready functions can be used in JavaScript by wrapping each one in an anonymous self-executing function.
---

**Contents**

[TOC]

# Section 1: jQuery

jQuery is a popular JavaScript library that simplifies the process of writing code for web browsers. It is well-known for its $(document).ready() function, which allows developers to execute code after the DOM (Document Object Model) is ready for manipulation.

# Section 2: $(document).ready()

The $(document).ready() function is a callback that is triggered when the DOM is completely ready for manipulation. This means that all HTML elements and their associated JavaScript objects are available for use. This is useful for ensuring that code is executed only after the page has been fully loaded.

# Section 3: Multiple $(document).ready()

It is possible to use multiple $(document).ready() functions in a single page. This is done by nesting the functions within each other. The innermost $(document).ready() function will be triggered first and the outermost $(document).ready() function will be triggered last.

# Section 4: Benefits

Using multiple $(document).ready() functions can be beneficial when writing complex JavaScript applications. It allows developers to separate code into logical chunks, which makes the code easier to read and maintain. Additionally, it can help to improve the overall performance of the application by ensuring that code is only executed when needed.
