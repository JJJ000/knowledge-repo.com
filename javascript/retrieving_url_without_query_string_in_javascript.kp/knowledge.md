---
title: What is the best way to obtain the url without the query string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, the URL.searchParams.get() method can be used to get the URL without query string in Javascript.
---

**Contents**

[TOC]

## Using the Location Object

The `location` object contains information about the current URL. The `location.href` property contains the entire URL, including the query string. To get the URL without the query string, you can use the `location.origin` property. This property returns the protocol, hostname, and port of the URL.

## Using the URL Object

The `URL` object is a newer API that allows you to parse and manipulate URLs. To get the URL without the query string, you can use the `URL.origin` property. This property returns the protocol, hostname, and port of the URL.

## Using Regular Expressions

You can also use regular expressions to extract the URL without the query string. The following regular expression will match the URL up to the query string:

```js
/^(.*?)\?/
```

## Using String Manipulation

You can also use string manipulation to extract the URL without the query string. You can use the `indexOf()` method to find the index of the first `?` character in the string. Then, you can use the `substring()` method to extract the URL up to the `?` character.
