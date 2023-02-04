---
title: Using javascript, store a cookie and then retrieve the cookie
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Set cookie document.cookie = `name=value`; Get cookie var cookieValue = document.cookie.split(`;`)[0].split(`=`)[1];
---

**Contents**

[TOC]

## Set cookie

Using JavaScript, you can set a cookie with the `document.cookie` property. The syntax for setting a cookie is as follows:

`document.cookie = "key1=value1;key2=value2;expires=date";`

Where `key1` and `value1` are the name and value of the cookie, respectively, and `date` is the expiration date of the cookie in UTC/GMT format.

## Get cookie

You can get a cookie using the `document.cookie` property. The syntax for getting a cookie is as follows:

`var x = document.cookie;`

Where `x` is a string containing a semicolon-separated list of all the cookies associated with the current document.

## Parse cookie

To parse the cookie string and get the value for a specific cookie, you can use the `split()` method to split the string into an array of name-value pairs. For example:

`var x = document.cookie.split(';');`

Where `x` is an array of strings containing the name-value pairs of each cookie.

## Retrieve value

Once you have the array of name-value pairs, you can use a loop to iterate over the array and find the cookie you are looking for. For example:

```
for (var i = 0; i < x.length; i++) {
    var pair = x[i].split('=');
    if (pair[0] == 'key1') {
        var value1 = pair[1];
    }
}
```

Where `value1` is the value of the cookie with the name `key1`.
