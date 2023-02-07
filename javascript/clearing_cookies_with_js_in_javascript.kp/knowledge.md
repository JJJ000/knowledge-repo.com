---
title: Removing all cookies using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: document.cookie = ``;
---

**Contents**

[TOC]

# Section 1: Retrieve All Cookies

The first step in clearing all cookies with JavaScript is to retrieve all cookies. This can be done using the `document.cookie` property. This property holds a string of all the cookies associated with the current document.

# Section 2: Parse the Cookie String

Once the cookie string is retrieved, it needs to be parsed in order to get the individual cookie names. This can be done using the `split()` method, which will split the cookie string into an array of strings, each containing a single cookie name.

# Section 3: Delete the Cookies

Once the individual cookie names are retrieved, they can be deleted using the `document.cookie` property. This property can be used to set an individual cookie's value to an empty string, which will delete the cookie.

# Section 4: Repeat for All Cookies

The process of retrieving, parsing, and deleting the cookies needs to be repeated for all the cookies associated with the document. This can be done using a loop, such as a `for` loop, to iterate over the array of cookie names. Once the loop is finished, all the cookies will have been deleted.
