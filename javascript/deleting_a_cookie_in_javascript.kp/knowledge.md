---
title: What is the process for removing a cookie?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To delete a cookie in Javascript, use the `document.cookie` property with an expiry date in the past.
---

**Contents**

[TOC]

# Section 1: Access the Cookie

The first step to deleting a cookie is to access the cookie. In JavaScript, you can access a cookie by using the `document.cookie` property. This property returns a string containing all the cookies for the current page.

# Section 2: Parse the Cookie String

The cookie string returned by `document.cookie` is a list of all the cookies for the page, separated by semicolons. To delete a specific cookie, you must parse the cookie string and find the cookie you want to delete.

# Section 3: Set the Cookie to Expire

Once you have identified the cookie you want to delete, you can set it to expire by setting its expiration date to a date in the past. You can do this by setting the `expires` property of the cookie to a date in the past.

# Section 4: Update the Cookie

Finally, you must update the cookie string by setting the `document.cookie` property with the modified cookie string. This will ensure that the browser deletes the cookie when it is next requested.
