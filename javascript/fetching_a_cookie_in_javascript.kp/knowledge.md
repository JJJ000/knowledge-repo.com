---
title: Retrieve cookie using its name
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The document.cookie property can be used to retrieve a cookie by name in JavaScript.
---

**Contents**

[TOC]

# Section 1: Initializing the Cookie

In order to get a cookie by name in Javascript, the cookie must first be initialized. This can be done by setting the cookie using the `document.cookie` property.

# Section 2: Setting the Cookie

To set the cookie, the `document.cookie` property must be assigned a string with the cookie name, value, and expiration time. This string should be formatted like the following:

`cookieName=cookieValue; expires=expirationTime;`

For example, to set a cookie called "username" with the value "JohnDoe" that expires after one day, the following string should be assigned to `document.cookie`:

`username=JohnDoe; expires=Fri, 22 May 2020 00:00:00 UTC;`

# Section 3: Retrieving the Cookie

Once the cookie is set, it can be retrieved by name using the `document.cookie` property. This property will return a string containing all of the cookies set for the current document. This string can then be parsed to find the cookie of interest.

# Section 4: Parsing the Cookie String

The cookie string returned by `document.cookie` can be parsed to find the cookie of interest. This can be done by splitting the string into an array of individual cookie strings and then looping through each cookie to find the one with the desired name. Once the cookie is found, its value can be retrieved.
