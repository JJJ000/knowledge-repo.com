---
title: How to utilize $(document).ready() with turbo-links in rails 4
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: $(document).ready() should be used with $(document).on(`turbolinksload`) to ensure that it runs after the turbolinks page load event.
---

**Contents**

[TOC]

# Introduction

Turbo-links is a feature of Rails 4 which allows for faster page loading by replacing full page reloads with partial page updates. This can be a great feature when used correctly, but it can also cause problems when trying to use certain JavaScript functions, such as `$(document).ready()`.

# Understanding $(document).ready()

`$(document).ready()` is a JavaScript function which is used to execute code as soon as the DOM is ready. This is typically used to ensure that all elements on the page are loaded before code is executed. Without `$(document).ready()`, code may be executed before elements are loaded, which can lead to unwanted behavior.

# Using $(document).ready() with Turbo-links

When using Turbo-links, `$(document).ready()` will not be triggered on page loads, as the page is not being fully reloaded. To get around this, you can use the `$(document).on('turbolinks:load', function() { // code here });` function instead. This will ensure that the code is executed every time a page is loaded with Turbo-links.

# Conclusion

Using `$(document).ready()` with Turbo-links can be tricky, but it is possible by using the `$(document).on('turbolinks:load', function() { // code here });` function. This will ensure that the code is executed every time a page is loaded with Turbo-links.
