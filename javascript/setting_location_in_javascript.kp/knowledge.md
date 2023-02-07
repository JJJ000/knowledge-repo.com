---
title: Comparing the use of location.href in JavaScript to the location object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Setting location.href will cause the browser to navigate to the new URL, while setting location will only update the current page`s URL.
---

**Contents**

[TOC]

# Setting location.href

The `location.href` property sets or returns the entire URL of the current page. This property can be used to get the current page address (URL) and to redirect the browser to a new page.

# Setting location

The `location` property sets or returns the location of the current window. This property can be used to get the current page address (URL) and to redirect the browser to a new page. It also allows you to access the current query string parameters and fragment identifier.

# Difference

The main difference between `location.href` and `location` is that `location.href` returns the entire URL of the current page, while `location` returns the location of the current window.

# Usage

Both `location.href` and `location` can be used to get the current page address (URL) and to redirect the browser to a new page. `location.href` is usually used when you want to get the entire URL of the current page, while `location` is usually used when you want to access the current query string parameters and fragment identifier.
