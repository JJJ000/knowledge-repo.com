---
title: Including a variable in the url using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can add a parameter to the URL with JavaScript by using the window.history.pushState() method.
---

**Contents**

[TOC]

### 1. Get the URL

To add a parameter to the URL with JavaScript, we first need to get the current URL. This can be done with the `window.location.href` property.

### 2. Add the Parameter

Next, we need to add the parameter to the URL. This can be done by using the `URLSearchParams` class. We can create a new instance of this class and pass in the current URL. Then, we can use the `set()` method to add the parameter to the URL.

### 3. Create the New URL

Once the parameter has been added, we can create the new URL by calling the `toString()` method on the `URLSearchParams` instance. This will return a string representation of the new URL with the parameter included.

### 4. Update the URL

Finally, we can update the URL by setting the `window.location.href` property to the new URL string. This will cause the page to be redirected to the new URL with the parameter included.
