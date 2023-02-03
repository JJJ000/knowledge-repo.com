---
title: What is the process for creating or removing a cookie using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To set a cookie with jQuery, use the $.cookie() method, and to unset a cookie, use the $.removeCookie() method.
---

**Contents**

[TOC]

Setting a Cookie with jQuery

1. Create a Cookie Object:

Create a cookie object that contains the name, value, and expiration date of the cookie.

```javascript
var cookie = {
    name: "cookieName",
    value: "cookieValue",
    expiration: new Date(Date.now() + 60 * 60 * 24 * 7) // 1 week
};
```

2. Set the Cookie:

Use the jQuery.cookie() method to set the cookie.

```javascript
$.cookie(cookie.name, cookie.value, { expires: cookie.expiration });
```

Unsetting a Cookie with jQuery

1. Unset the Cookie:

Use the jQuery.removeCookie() method to unset the cookie.

```javascript
$.removeCookie(cookie.name);
```
