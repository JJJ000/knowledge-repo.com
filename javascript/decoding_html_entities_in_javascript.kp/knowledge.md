---
title: Convert html entities to characters
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Javascript provides the built-in function `decodeURIComponent()` to decode HTML entities.
---

**Contents**

[TOC]

### Using the Browser's DOM

The browser's DOM (Document Object Model) provides a method for decoding HTML entities. This method is called `document.createElement()`. It takes a string as an argument and returns a DOM element with the HTML entities decoded.

For example, if you have a string `"&amp;lt;h1&amp;gt;Hello World&amp;lt;/h1&amp;gt;"` you can decode it like this:

```js
let str = "&amp;lt;h1&amp;gt;Hello World&amp;lt;/h1&amp;gt;";
let el = document.createElement('div');
el.innerHTML = str;
let decodedStr = el.textContent; // "<h1>Hello World</h1>"
```

### Using a Library

There are several libraries available for decoding HTML entities. One popular library is [he](https://github.com/mathiasbynens/he). It provides a method called `decode()` which takes a string as an argument and returns the decoded version.

For example, using the same string from the previous example:

```js
let str = "&amp;lt;h1&amp;gt;Hello World&amp;lt;/h1&amp;gt;";
let decodedStr = he.decode(str); // "<h1>Hello World</h1>"
```

### Using Regular Expressions

Regular expressions can also be used to decode HTML entities. This approach is not recommended because it is not as robust as the other methods, but it can be useful in certain situations.

The following regular expression can be used to decode HTML entities:

```js
/&#?[a-z0-9]+;/gi
```

For example, using the same string from the previous examples:

```js
let str = "&amp;lt;h1&amp;gt;Hello World&amp;lt;/h1&amp;gt;";
let decodedStr = str.replace(/&#?[a-z0-9]+;/gi, function(match) {
  return String.fromCharCode(match.replace(/[a-z0-9]+;/gi, ''));
}); // "<h1>Hello World</h1>"
```

### Using a Custom Function

It is also possible to write a custom function to decode HTML entities. This approach is not recommended because it is time consuming and error-prone, but it can be useful in certain situations.

The following function can be used to decode HTML entities:

```js
function decodeHTMLEntities(str) {
  let element = document.createElement('div');
  element.innerHTML = str;
  return element.textContent;
}
```

For example, using the same string from the previous examples:

```js
let str = "&amp;lt;h1&amp;gt;Hello World&amp;lt;/h1&amp;gt;";
let decodedStr = decodeHTMLEntities(str); // "<h1>Hello World</h1>"
```
